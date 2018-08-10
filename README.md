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
| api_url          |  url api <br/> *Type : String*                      |
| _config         |     **_config: IBApiConfig**                   |



#### Methods
| Methods       | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| findAll          |   **findAll(params: any)** <br/> get all data  <br/> *Type: any*                                                                                       |
| findAllODataQuery |      **findAllODataQuery(params: ODataQuery):Observable<T[]>** ,<br/> get all data <br/> *Type: Observable*                  |
| search            |    **search (data: any,api_search_name: string):Observable<T[]>** <br/> get all data    <br/> *Type: Observable*                   |
| find   |  **find(id: any): Observable<T>** <br/> get data by id <br/> *Type: Observable* |
| update        |  **update(id: any, data: any)** <br/> update data by id <br/> *Type: any*                                                                                       |
| insert  | **insert(data: any)** <br/> insert data   <br/> *Type: any*                        |
| delete      |  **delete(data: any)** <br/> delete data by id  <br/> *Type: any*                                  |
| generateParam     | **generateParam(params: any)** <br/> generate paramater in any type                  |
| generateParamODataQuery |**generateParamODataQuery(query: ODataQuery)** <br/> generate a paramater that can be used to modify an ODataQuery in the query string of the request URI                            |
| processData        |    **processData(res: Response)** <br/> response data type json                 |
| handleError      |    **handleError(error: any)** <br/> handle any error that occurred <br/> *Type: any*                  |


### ApiConfig
 `Class`

#### Properties
| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| config            |  <br/> *Type : any*                                                                                          |
| urlAPI           |  <br/> *Type : String*                                                                                          |
| headers            |  <br/> *Type : any*                                                                                          |
| methods            | <br/> **defaultMethods: MethodHttp**                                                                                         |
| query            |  get all data<br/> *Type : String*                                                                                          |
| update           |  update data<br/> *Type : String*                      |
| insert          |   insert data<br/> *Type : String*                      |
| delete | delete data<br/> *Type: String*                           |

#### Methods
| Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| getConfig            |  get API URL                                                                                          |

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
  `Class`
  
   #### Selector
   moo-vform

   #### Properties

| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| modelSchema        |  **modelSchema: Dictionary<Field>**                                                                                 |
| onSubmit        |        *Type: any*                                                                                 |
| ngForm       |        **ngForm: NgForm**                                                                                 |

   #### Methods

  | Methods    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
|     formSubmit        |    **formSubmit ( f: NgForm)**<br/> a method that is submitted from NgForm                                                                       |
|    ngAfterViewInit    |     A callback method that is invoked immediately after Angular has completed initialization of a component's view. It is invoked only once when the view is instantiated.                                                                      |
|        ngOnInit       |      A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                                                                     |   
 
  ### MooField
  `Class`
   #### Selector 
   moo-field

   #### Properties
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| config         |   **config: Field**<br/>schema <br/>                                                                 |
| name         |  <br/>*Type: String*<br/>                                                                    |
| form   |     **form: MooVformComponent**<br/>                                                             |
| _stringFieldInputTypes  |    **_stringFieldInputTypes: string[]**<br/>*Type: String* <br/>text,number,textarea, email password                                                        |
| isStringField   |     **isStringField(): boolean**<br/>                                                             |
| field   |                                                                  |
   
   #### Methods
   ngOnInit

  ### MooFieldStringComponent
   #### Selector
   moo-field-string
   
   #### Properties

   | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| model      |  **model: NgModel** <br/>                                                                   |
| value       |  <br/>*Type: String*                                                                    |
| name        |  <br/>*Type: String*                                                                    |
| config       |  <br/>*Type: StringField*                                                                   |

| _hasError       |  <br/>*Type: StringField*                                                                   | 

| _errorMessage       |  <br/>*Type: any*                                                                   | 
| required       |  String input is required<br/>                                                                   | 
| minlength    | Has min lenght<br/>                                                                   | 
| _istTextArea       |  <br/>*Type: boolean*                                                                   | 

  #### Methods
   | Methods    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| ngOnInit    |                                                                    |
| ngAfterViewInit     |  <br/>*Type: String*                                                                    |

### Fields
 `Class`
 #### Methods
 | Methods  | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| textField   |    **textField(c: Partial<StringField>): StringField**<br/>*Type: Partial*                                                           |
| hiddenField     |  **hiddenField(c: Partial<HiddenField>): HiddenField**<br/>*Type: Partial*                                                                    |
| radioField   |  **radioField(c: Partial<BooleanField>): BooleanField**<br/>*Type: Partial*                                                                    |
### Field
 `Interface`

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| inputType    |    <br/>*Type: String*                                                           |
| model     |  <br/>*Type: String*                                                                    |
| required    |  <br/>*Type: boolean*                                                                    |
### StringField
 `Interface`

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| placeholder    |      <br/>*Type: String*                                                           |
| label     |  <br/>*Type: String*                                                                    |
| minlength   |  <br/>*Type: number*                                                                    |
| maxlength   |  <br/>*Type: number*                                                                    |

### BooleanField
 `Interface`

#### Properties
| Properties    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| checked   |      *checked: true* <br/>                                                          |

### HiddenField
 `Interface`








 ### List View
  #### MooVList Sequence Diagram
  
  ### MooVList  
   #### Selector
   app-moo-vlist

= 
 ### Table View
  #### MooVTable Sequence Diagram
  ### MooVTable
   #### Selector
   moo-vtable



   #### Properties
  
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| columns          |  **columns: Field []**<br/> initialize field in array                                                                                         |
| _dataSource$          |   initialize variabel  <br/>*Type observable*                       |
| _modelSchema      |  | **_modelSchema:Dictionary<Field>**<br/>Schema                |


   #### Methods
  
    
  | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| setDataSource()          |    **setDataSource(data: Observable<any>)**<br/> set new  datasource                                                                                    |
| setSchema()          |   **setSchema(schema: any)**<br/>  set new Schema                       |
| ngOnInit     |  |   A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                       |

   
  ### Field
  `Interface`
   Abstraction for hold configuration
   #### Properties
| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| inputType           |  <br/> *Type : String*                                                                                          |
| model           |  <br/> *Type : String*                      |
| required          |   declare the Field is required or not <br/> *Type : Boolean*                      |





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

<https://github.com/>


- **Oriani**

<https://github.com/orianisihaloho>

- **Felix**

<https://github.com/felixsiburian>




