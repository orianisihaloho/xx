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
### Form View
Add tag `moo-vform` <moo-vform> on template Core UI
### Table View
Add tag `moo-vtable` on template Core UI
### List View
Add tag `moo-vlist` on template Core UI

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

## Active Record

Active Record is a helper library for connect API in your client Angular 4 Application.

### Active Record
`Class`  
A class that contains modelSchema, URL API and some method CRUD data. 

#### Properties
| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| modelSchema           |  **modelSchema: Dictionary<Field> = {}**<br/> Schema for fields based on your requirements of fields . Set on Contact Service.                                           |
| api_url          |  URL for connect to API. Set on Contact Service <br/> *Type : String*                      |
| _config         |     Variable name of interface IBApiConfig. **_config: IBApiConfig**                   |

#### Methods
| Methods       | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| findAll          |   **findAll(params: any)** <br/> Get all data  <br/> *Type: any*                                                                                       |
| findAllODataQuery |      **findAllODataQuery(params: ODataQuery):Observable<T[]>** ,<br/> Get all data <br/> *Type: Observable*                  |
| search            |    **search (data: any,api_search_name: string):Observable<T[]>** <br/> Search <br/> *Type: Observable*                   |
| find   |  **find(id: any): Observable<T>** <br/> Get data by id <br/> *Type: Observable* |
| update        |  **update(id: any, data: any)** <br/> Update data by id <br/> *Type: any*                                                                                       |
| insert  | **insert(data: any)** <br/> Insert data   <br/> *Type: any*                        |
| delete      |  **delete(data: any)** <br/> Delete data by id  <br/> *Type: any*                                  |
| generateParam     | **generateParam(params: any)** <br/> Generate paramater in any type                  |
| generateParamODataQuery |**generateParamODataQuery(query: ODataQuery)** <br/> Generate a paramater that can be used to modify an ODataQuery in the query string of the request URI                            |
| processData        |    **processData(res: Response)** <br/> Response data json                 |
| handleError      |    **handleError(error: any)** <br/> Handle any error that occurred <br/> *Type: any*                  |


### ApiConfig
 `Class`
A class that contains 
#### Properties
| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| config            |  Variable name to config API, headers and methods *Type : any*                                                                                          |
| urlAPI           |  Variable name of URL API *Type : String*                                                                                          |
| headers            |  *Type : any*                                                                                          |
| methods            | **defaultMethods: MethodHttp**                                                                                         |
| query            |  Get all data<br/> *Type : String*                                                                                          |
| update           |  Update data<br/> *Type : String*                      |
| insert          |   Insert data<br/> *Type : String*                      |
| delete | Delete data<br/> *Type: String*                           |

#### Methods
| Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| getConfig            | **getConfig()**<br/> Return configuration of URL API, headers and methods                                                                                          |

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
### Contact Service
`Injectable`
A service to set URL API and model schema of fields as needed.
#### Properties
| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| api_url          |  URL for connect to API <br/> *Type : String*                      |
| modelSchema           |  **modelSchema[]** <br/> Schema for fields based on your requirement of fields.                                             |

## Views
 ### Form View
 Display view in form.
  ### MooVForm
  `Component` <br/>
  A component that makes it easy to create form.
  
   #### Selector
   moo-vform

   #### Properties

| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| modelSchema        |  **modelSchema: Dictionary<Field>**Schema for fields based on your requirements of fields .                                                                                |
| @Input(onSubmit)        |      The @Input decorator with a variable name as `onSubmit` to pass data from MooVFormcComponent. Use to bind the element in the template. <br/> *Type: any*                                                                                 |
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
  The MooField directive represents an individual field with variable `name`as name of field.

   #### Selector 
   moo-field

   #### Inputs
   | Input    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| name        |    The name of field<br/>*Type: String*.                                                               |
  
   #### Properties
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| config         |   **config: Field**<br/> Schema for field <br/>                                                                 |
|@Input(name)         |  The @Input decorator with a variable name as `name` to pass data from component. Use to bind the element in the template. <br/>*Type: String*                                                                    |
| _stringFieldInputTypes  |    **_stringFieldInputTypes: string[]**<br/> Type of input for String Field in array. There are text, number, textarea, email, and password. <br/>*Type: String*                                                     |
| form   |  **form: MooVformComponent**<br/>Initialize dependencies of MooVformComponent on property name `form`                                                                |

   #### Methods
 | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| isStringField   |   **get isStringField(): boolean**<br/> Return _stringFieldInputTypes                                                              |
|  ngOnInit    |   A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.<br/>*Return modelSchema.*                                                                             |

   
  ### MooFieldStringComponent
   `Component`
   #### Selector
   moo-field-string
   
   #### Properties
   | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| @ViewChild(model)      |  **model: NgModel** <br/>Query for a VIEW child of type NgModel                                                                 |
| value       |  Variable to get the value of field. View on readonly mode. *Type: String*                                                                    |
| _config       |  Initialize variable name `_config` for interface StringField.                                                                  |
| _hasError       |   Whether Field has error <br/>*Type: boolean*                                                                   | 
| _errorMessage       |  Initialize variable name `_errorMessage` for error message in input type such as required, minimal length of input, and email pattern.           <br/>*Type: any*                                                                   | 
| required       | Whether Field is required.                                                                   | 
| minlength    | String has min length.                                                                  | 
| emailPattern   | Check  email pattern in String input.                                                                  || field   |       Initialize dependencies of MooFieldComponent on property name `field`.                                                                | 
  #### Methods
   | Methods    | Description                                                                                                  |
| ---------         | -----------                                                                                                           |
| _istTextArea       |  **get isTextArea()**<br/>Check whether inputType is text area.<br/>*Type: boolean* | 
| ngOnInit       |  A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.<br/>*Return _config as StringField.*      | 
| ngAfterViewInit       |  A callback method that is invoked immediately after Angular has completed initialization of a component's view. It is invoked only once when the view is instantiated.<br/>*Return model* | 


### Fields
 `Class`
 A class to declare field types (texField, hiddenField, and radioField).

 #### Methods
 | Methods  | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| textField   |    **textField(c: Partial<StringField>): StringField**<br/>Return field types as StringField.<br/>*Type: Partial*                                                           |
| hiddenField     |  **hiddenField(c: Partial<HiddenField>): HiddenField**<br/>Return field types as HiddenField.<br/>*Type: Partial*                                                                    |
| radioField   |  **radioField(c: Partial<BooleanField>): BooleanField**<br/>Return field types as BooleanField.<br/>*Type: Partial*                                                                    |
### Field
 `Interface`   
 Abstraction for hold configuration.

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| inputType    |    Type of input.<br/> *Type: String*<br/>                                                           |
| model     | *Type: String* <br/>                                                                   |
| required    |  Whether the Field is required.<br/>*Type: boolean*                                                                    |
### StringField
 `Interface`
Set field for StringField.
#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| placeholder    |    Text in the input field<br/>*Type: String*<br/>                                                           |
| label     |  Text.<br/>*Type: String*<br/>                                                                    |
| minlength   |  String Input has min length.<br/>*Type: number* <br/>                                                                   |
| maxlength   |  String Input has max length.<br/>*Type: number*<br/>                                                                    |
| pattern  |  String Input has pattern.<br/>*Type: number*<br/>                                                                    |
| row  |   Size of row on text area field.<br/> *Type: number*<br/>                                                                    |
| col   |  Size of col on text area field.<br/>*Type: number*<br/>                                                                    |
### BooleanField
 `Interface`
 Set field for BooleanField.

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| checked   |     **checked: true** <br/>                                                          |

### HiddenField
 `Interface`
 Set field for Hidden Field.

 ### List View
  Display view in list.
  ### MooVList 
  `Component`
  A component that makes it easy to create list
   
   #### Selector
   moo-vlist

  #### Properties
  
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| _dataSource$          |  *Type Observable*                       |
| _modelSchema      |  |**_modelSchema:Dictionary<Field>**<br/>Schema                |

  #### Methods
  
  | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| setDataSource         |   **setDataSource(data: Observable<any>)**<br/>*Type: Observable*                       |
| setSchema         |   **setSchema(schema: any)**<br/>Schema                       |
| ngOnInit        | **ngOnInit()**<br/>A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                         |


### NgTemplate
  `Directive`
  The NgTemplate directive represents an individual list

 ### Table View
  Display view in table.
  ### MooVTable
  `Component`
   A component that makes it easy to create table
   #### Selector
   moo-vtable

   #### Input
  
   #### Properties
  
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| columns          |  **columns: Field []**<br/> Field in array                                                                                    |
| _dataSource$          | *Type observable*                       |
| _modelSchema         | **_modelSchema:Dictionary<Field>**<br/>Schema                       |


   #### Methods
 
  | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| setDataSource()          |    **setDataSource(data: Observable<any>)**<br/> Set new  datasource                                                                                    |
| setSchema()          |   **setSchema(schema: any)**<br/>  Set new Schema                       |
| ngOnInit()          |    A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.             |

 ### Chart View 
  ### MooVChart
   #### Selector
   moo-vchart

 ### Report View   
   ### MooVReport
   #### Selector
   moo-vreport


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




