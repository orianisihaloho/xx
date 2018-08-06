# Mooadmin-coreui-ngx
Mooadmin Core UI is extended shared library for Core UI, focused on view such as Form, Table, Report & Chart

## Table of Contents
* [Getting Started](#getting-started)
* [Usage](#usage)
* [What's included](#whats-included)
* [Active Record](#active-record)
* [Views](#Views)
* [Fom View](#form-view)
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
|       ├── service
|           ├── contact.service.ts
|           ├── pagerService.ts
|           └── ...
|       ├── views
|       └── ...
│   ├── assets/
│   ├── environments/
|   ├── lib
|       ├── Views
|           ├── form-view
|               ├── moofield/
|               ├── mooform/
|       ├── active-record   
│   ├── scss/
│   ├── index.html
│   └── ...
├── .angular-cli.json
├── ...
├── package.json
└── ...
```
## Active Record

Active Record is a helper library for connect API in your Angular 4 Application.

### Active Record
 Class   

| Methods       | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| `findAll(params: any)`            |                                                                                            |
| `search (data: any,api_search_name: string)`           |                           |
| `find(id: any)`       |  |
| `update(id: any)  `       |                                                                                          |
| `insert(data: any) ` |                            |
| `delete(id: any)  `       |                                    |
| `generateParam(params: any) `      |                   |
| `processData(res: Response)  `      |                     |
| `handleError(error: any)  `      |                        |


### ApiConfig
 Interface

| Properties     | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
| `query`            |                                                                                            |
| `update`           |                           |
| `insert`       |  |
| `delete` |                            |


## Views
 ### Form View
 #### MooField
 Component
 ##### Selector 
 moo-field
 ##### Input
 ngSwithCase
 
| Input    | Description                                                                                                           |
| ---------         | -----------                                                                                                           |
|  ngSwithCase =  "Text"       |                                                                                            |
| ngSwithCase =  "Number"             |                           |
| ngSwithCase =  "Email"         |  |
| ngSwithCase =  "Password"   |  |
| ngSwithCase =  "Radio"         |  |
| ngSwithCase =  "Checkbox"   |  |



 #### Moooform
 Component
 ##### Selector
 moo-vform










 ### List View
 ### Table View
 ### Chart View
 ### Report View


## Creators
- **Affandy Lamusu**

<https://github.com/afandylamusu>

- **Andrey**

<https://github.com/>


- **Ronald**

<https://github.com/>


- **Oriani**

<https://github.com/orianisihaloho>

- **Felix**

<https://github.com/>




