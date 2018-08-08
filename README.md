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
├── dist/
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

| Methods       | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| findAll          |   **findAll(params: any)** <br/> get all data  <br/> *Type: any*                                                                                       |
| findAllODataQuery |      **findAllODataQuery(params: ODataQuery):Observable<T[]>** ,<br/> get all data <br/> *Type: Observable*                  |
| search            |    **search (data: any,api_search_name: string):Observable<T[]>** <br/> get all data    <br/> *Type: Observable*                   |
| find   |  **find(id: any): Observable<T>** <br/> get data by id <br/> *Type: Observable* |
| update        |  **update(id: any, data: any)** <br/> update data by id <br/> *Type: any                                                                                       |
| insert  | **insert(data: any)** <br/> insert data   <br/> *Type: any*                        |
| delete      |  **delete(data: any)** <br/> delete data by id  <br/> *Type :any*                                  |
| generateParam     | **generateParam(params: any)** <br/> generate paramater in any type                  |
| generateParamODataQuery |**generateParamODataQuery(query: ODataQuery)** <br/> generate a paramater that can be used to modify an ODataQuery in the query string of the request URI                            |
| processData        |    **processData(res: Response)** <br/> response data type json                 |
| handleError      |    **handleError(error: any)** <br/> handle any error that occurred <br/> *Type: any*                  |


### ApiConfig
 `Interface`

| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| query            |  get all data<br/> *Type : String*                                                                                          |
| update           |  update data<br/> *Type : String*                      |
| insert          |   insert data<br/> *Type : String*                      |
| delete | delete data<br/> *Type: String*                           |


## Views
 ### Form View
  ### MooVForm
  `Class`
  
   #### Selector
   moo-vform

   #### Properties
   modelSchema: Dictionary
   onSubmit: any 

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
| config         |   schema <br/>*Type: any*                                                                  |
| name         |  <br/>*Type: any*<br/>                                                                    |
| form   |     **form: MooVformComponent**<br/>                                                             |

   #### Methods
   ngOnInit

  ### MooFieldStringComponent
   #### Selector
   moo-field-string
   
   #### Properties

   | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| name        |  <br/>*Type: String*                                                                    |
| config       |  <br/>*Type: StringField*                                                                   |
 
 ### List View
  ### MooVList  
   #### Selector
   app-moo-vlist


 ### Table View
  ### MooVTable
   #### Selector
   moo-vtable



   #### Properties
  
  | Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| columns          |  **columns: Field []**<br/> initialize field in array                                                                                         |
| _dataSource$          |   initialize variabel  <br/>*Type observable*                       |
| _modelSchema      |  |      **_modelSchema: Dictionary<Field>**<br/>Schema                |


   #### Methods
  
    
  | Methods     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| setDataSource()          |    **setDataSource(data: Observable<any>)**<br/> set new  datasource                                                                                    |
| setSchema()          |   **setSchema(schema: any)**<br/>  set new Schema                       |
| ngOnInit     |  |       A callback method that is invoked immediately after the default change detector has checked the directive's data-bound properties for the first time, and before any of the view or content children have been checked. It is invoked only once when the directive is instantiated.                    |

   
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
  ### MooVChart
   #### Selector
   app-moo-vchart


 ### Report View


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




