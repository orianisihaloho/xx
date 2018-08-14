# Mooadmin-coreui-ngx
Mooadmin Core UI is extended shared library for Core UI, focused on view such as Form, Table, Report & Chart.

## Table of Contents
* [Getting Started](#getting-started)
* [Usage](#usage)
* [What's included](#whats-included)
* [Active Record](#active-record)
* [Views](#Views)
* [Form View](#form-view)
* [List View](#list-view)
* [Table View](#table-view)
* [Chart View](#chart-view)
* [Report View](#report-view)
* [Creators](#creators)

## Getting Started
### Installation

``` bash
# clone the repo
$ git clone 
https://github.com/afandylamusu/mooadmin-coreui-ngx.git 

# go into app's directory
$ cd mooadmin-coreui-ngx

# install app's dependencies
$ npm install
```

## Usage

``` bash
# serve with hot reload at localhost:4200.
$ ng serve

# build for production with minification
$ ng build
```
## What's included
Within the download you'll find the following directories and files, logically grouping common assets and providing both compiled and minified variations. You'll see something like this:

```
mooadmin-coreui-ngx/
├── .vscode/
├── e2e/
├── FProject/
├── node_modules/
├── src/
│   ├── app
|       ├── containers/
|       ├── views
|           ├── mooadmin
|               ├── contact
|                   ├── contact.component
|               ├── moo-demo-routing.module
|               ├── moo-demo.module
|               └── ...
|          └── ...
|       ├── app.component
|       ├── app.module
|       ├── app.routing
|       └── ...
│   ├── assets/
│   ├── environments/
|   ├── lib
|       ├── mooadmin-ngx
|           ├── moo-field
|               ├── moo-field.component
|               ├── moo-field-string.component
|           ├── moo-vchart/
|               ├── moo-vchart.component
|           ├── moo-vform/
|               ├── moo-vform.component
|           ├── moo-vlist/
|               ├── moo-vlist.component
|           ├── moo-vtable/
|               ├── moo-table.component
|           ├── active-record
|           ├── dictionary
|           ├── field-types
|           ├── mooadmin.module   
│   ├── scss/
|   ├── services
|       ├── contact.service
|       ├── contact
│   ├── index.html
│   └── ...
├── .angular.json
├── ...
├── package.json
└── ...
```

## Class Diagram


## Active Record

Active Record is a helper library for connect API in your client Angular 4 Application.

### Active Record
`Class`  
#### Properties
| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| modelSchema           |   **modelSchema: Dictionary<Field> = {}**                                                                                         |
| api_url          |  URL API <br/> *Type : String*                      |
| _config         |     **_config: IBApiConfig**                   |


#### Methods
| Methods       | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| findAll          |   **findAll(params: any)** <br/> Get all data  <br/> *Type: any*                                                                                       |
| findAllODataQuery |      **findAllODataQuery(params: ODataQuery):Observable<T[]>** ,<br/> Get all data <br/> *Type: Observable*                  |
| search            |    **search (data: any,api_search_name: string):Observable<T[]>** <br/> Get all data    <br/> *Type: Observable*                   |
| find   |  **find(id: any): Observable<T>** <br/> Get data by id <br/> *Type: Observable* |
| update        |  **update(id: any, data: any)** <br/> Update data by id <br/> *Type: any*                                                                                       |
| insert  | **insert(data: any)** <br/> Insert data   <br/> *Type: any*                        |
| delete      |  **delete(data: any)** <br/> Delete data by id  <br/> *Type: any*                                  |
| generateParam     | **generateParam(params: any)** <br/> Generate paramater in any type                  |
| generateParamODataQuery |**generateParamODataQuery(query: ODataQuery)** <br/> Generate a paramater that can be used to modify an ODataQuery in the query string of the request URI                            |
| processData        |    **processData(res: Response)** <br/> Response data type json                 |
| handleError      |    **handleError(error: any)** <br/> Handle any error that occurred <br/> *Type: any*                  |


### ApiConfig
 `Class`

#### Properties
| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| config            |  *Type : any*                                                                                          |
| urlAPI           |  *Type : String*                                                                                          |
| headers            |  *Type : any*                                                                                          |
| methods            | **defaultMethods: MethodHttp**                                                                                         |
| query            |  Get all data<br/> *Type : String*                                                                                          |
| update           |  Update data<br/> *Type : String*                      |
| insert          |   Insert data<br/> *Type : String*                      |
| delete | Delete data<br/> *Type: String*                           |

#### Methods
| Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| getConfig            | **getConfig()**<br/> Return configuration API URL, headers and methods                                                                                          |

### IBAConfig
 `Interface`
 #### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| urlAPI           |        *Type : String*                                                                                 |
| headers           |        *Type : any*                                                                                 |
| methods           |        **methods: MethodHttp**                                                                              |

### MethodHttp
 `Interface`
 #### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| query          |        *Type : String*                                                                                 |
| update          |        *Type : String*                                                                                 |
| insert          |       *Type : String*                                                                               |
| delete          |        *Type : String*                                                                               |
| method: String          |      *Type : String*                                                                               |


### ODataQuery
 `Interface`

 #### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| top         |        *Type : number*                                                                                 |
| skip         |        *Type : number*                                                                                 |
| filter          |       *Type : String*                                                                               |
| expand         |        *Type : String*                                                                               |


## Views
 ### Form View
  #### MooVForm Sequence Diagram

  ### MooVForm
  `Component` <br/>
  A component that makes it easy to create form
  
   #### Selector
   moo-vform

   #### Properties

| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| modelSchema        |  **modelSchema: Dictionary<Field>**                                                                                 |
| @Input(onSubmit)        |      The @Input decorator with a variable name as `onSubmit` to pass data from component. Use to bind the element in the template. <br/> *Type: any*                                                                                 |
| @ViewChild(ngForm)       |    **ngForm: NgForm** <br/>Query for a VIEW child of type NgForm                                                             |

   #### Methods

  | Methods    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
|     formSubmit        |    **formSubmit ( f: NgForm)**<br/> A method that is submitted from NgForm . There is postContact() with property (id,name,number).                                                                  |
|     postContact      |    **postContact ( contact: Contact)**<br/> A method to insert data contact.                                                                 |
|    ngAfterViewInit    |     A callback method that is invoked immediately after Angular has completed initialization of a component's view. It is invoked only once when the view is instantiated.                                                                      |
|        ngOnInit       |      A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                                                                     |   
 
  ### MooField
  `Directive`
  The MooField directive represents an individal field with variable `name`as name of field

   #### Selector 
   moo-field

   #### Inputs
   | Input    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| name        |    The name of field*Type: String*<br/>                                                                 |
  
   #### Properties
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| config         |   **config: Field**<br/> Schema for field <br/>                                                                 |
|@Input(name)         |  The @Input decorator with a variable name as `name` to pass data from component. Use to bind the element in the template <br/>*Type: String*                                                                    |
| _stringFieldInputTypes  |    **_stringFieldInputTypes: string[]**<br/> Type of input for String Field in array. There are text, number, textarea, email, and password <br/>*Type: String*                                                     |
| form   |  **form: MooVformComponent**<br/>initialize dependencies of MooVformComponent on property name `form`                                                                |

   #### Methods
 | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| isStringField   |   **get isStringField(): boolean**<br/> return _stringFieldInputTypes                                                              |
|  ngOnInit    |   A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                                                                             |

   
  ### MooFieldStringComponent
   #### Selector
   moo-field-string
   
   #### Properties
   | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| @ViewChild(model)      |  **model: NgModel** <br/>Query for a VIEW child of type NgModel                                                                 |
| value       |  *Type: String*                                                                    |
| _config       |  initialize variable name `_config` for StringField                                                                   |
| _hasError       |   whether Field has error <br/>*Type: boolean*                                                                   | 
| _errorMessage       |  initialize variable name `_errorMessage` for error message in input type such as required, minlength of input, and email pattern           <br/>*Type: any*                                                                   | 
| required       | whether Field is required                                                                   | 
| minlength    | String Has min length                                                                  | 
| emailPattern   | check  email pattern in String input                                                                  || field   |       initialize dependencies of MooFieldComponent on property name `field`                                                                | 
  #### Methods
   | Methods    | Description                                                                                                  |
| ---------         | -----------                                                                                                           |
| _istTextArea       |  **get isTextArea()**<br/>check wheter inputType is text area <br/>*Type: boolean* | 
| ngOnInit       |  A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.     | 
| ngAfterViewInit       |  A callback method that is invoked immediately after Angular has completed initialization of a component's view. It is invoked only once when the view is instantiated. | 


### Fields
 `Class`
 A class to declare field types (texfield, hidden field, radiofield)
 #### Methods
 | Methods  | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| textField   |    **textField(c: Partial<StringField>): StringField**<br/>Return input as StringField <br/>*Type: Partial*                                                           |
| hiddenField     |  **hiddenField(c: Partial<HiddenField>): HiddenField**<br/>Return input as HiddenField<br/>*Type: Partial*                                                                    |
| radioField   |  **radioField(c: Partial<BooleanField>): BooleanField**<br/>Return input as BooleanField*Type: Partial*                                                                    |
### Field
 `Interface`   Abstraction for hold configuration

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| inputType    |    Type of input *Type: String*<br/>                                                           |
| model     | *Type: String* <br/>                                                                   |
| required    |  whether the Field is required  <br/>*Type: boolean*                                                                    |
### StringField
 `Interface`

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| placeholder    |    Text in the input field *Type: String*<br/>                                                           |
| label     |  Text title *Type: String*<br/>                                                                    |
| minlength   |  String Input has min length<br/>*Type: number* <br/>                                                                   |
| maxlength   |  String Input has max length<br/>*Type: number*<br/>                                                                    |
| pattern  |  String Input has pattern<br/>*Type: number*<br/>                                                                    |
| row  |   size of text area field *Type: number*<br/>                                                                    |
| col   |  size of text area field *Type: number*<br/>                                                                    |
### BooleanField
 `Interface`

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| checked   |      **checked: true** <br/>                                                          |

### HiddenField
 `Interface`

 ### List View
  #### MooVList Sequence Diagram
  
  ### MooVList 
  `Component`
  A component that makes it easy to create list
   
   #### Selector
   moo-vlist

  #### Properties
  
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| _dataSource$          |  Variabel name  <br/>*Type Observable*                       |
| _modelSchema      |  | **_modelSchema:Dictionary<Field>**<br/>Schema                |

  #### Methods
  
  | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| setDataSource         |   **setDataSource(data: Observable<any>)**<br/>*Type Observable*                       |
| setSchema      |  | **setSchema(schema: any)**<br/>Schema                |
| ngOnInit     |  | **ngOnInit()**<br/>  A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                   |

### NgTemplate
  `Directive`
  The NgTemplate directive represents an individuaal list


 ### Table View
  #### MooVTable Sequence Diagram

  ### MooVTable
  `Component`
   A component that makes it easy to create table
   #### Selector
   moo-vtable


   #### Properties
  
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| columns          |  **columns: Field []**<br/>Initialize field in array                                                                                         |
| _dataSource$          | *Type observable*                       |
| _modelSchema      |  | **_modelSchema:Dictionary<Field>**<br/>Schema                |


   #### Methods
  
    
  | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| setDataSource()          |    **setDataSource(data: Observable<any>)**<br/> Set new  datasource                                                                                    |
| setSchema()          |   **setSchema(schema: any)**<br/>  Set new Schema                       |
| ngOnInit     |  |   A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                       |

 ### Chart View
  #### MooVChart Sequence Diagram
  
  ### MooVChart
   #### Selector
   app-moo-vchart

 ### Report View
  #### MooVReport Sequence Diagram


## Creators
- **Affandy Lamusu**

<https://github.com/afandylamusu>

- **Andrey**

<https://github.com/andreycls>


- **Ronald**

<https://github.com/ronald1402>


- **Oriani**

<https://github.com/orianisihaloho>

- **Felix**

<https://github.com/felixsiburian>




