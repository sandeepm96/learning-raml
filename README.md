# Learning RAML

RAML for dummy API

### Resources of API
```
GET /v1/foos
POST /v1/foos
GET /v1/foos/{id}
PUT /v1/foos/{id}
DELETE /v1/foos/{id}
GET /v1/foos/name/{name}
GET /v1/foos?name={name}&ownerName={ownerName}
```

#### Generating HTML Documentation
HTML documentation can be generated from the raml file by using the Node.js library [raml2html](https://www.npmjs.com/package/raml2html).

### Prerequisites
1. [Node.js](https://nodejs.org/en/)
2. [npm](https://www.npmjs.com/get-npm)

### Install
```
npm i -g raml2html
```

### Usage
##### As a command line script
```
raml2html api.raml > api.html
```

##### As a library
```
const raml2html = require('raml2html');
const configWithDefaultTheme = raml2html.getConfigForTheme();

// source can either be a filename, url, or parsed RAML object
raml2html.render(source, configWithDefaultTheme).then(function(result) {
  // Save the result to a file or do something else with the result
}, function(error) {
  // Output error
});
```

### HTML Documentation View
##### Overview
![Overview](/screenshots/index.png)
##### Request View of Specific Resource
![Overview](/screenshots/request.png)
##### Response View of Specific Resource
![Overview](/screenshots/response.png)
