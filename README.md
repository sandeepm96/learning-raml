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

### Generating HTML Documentation
HTML documentation can be generated from the raml file by using the following packages:

## raml2html
A simple RAML to HTML documentation generator, written for Node.js, with theme support.

### Prerequisites
1. [Node.js](https://nodejs.org/en/)
2. [npm](https://www.npmjs.com/get-npm)

### Install
```
$ npm i -g raml2html
```

### Usage
##### As a command line script
```
$ raml2html api.raml > api.html
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

## api-console
An API console for RAML (Restful Api Modeling Language) documents. The RAML Console allows browsing of API documentation and in-browser testing of API methods.

### Prerequisites
1. [Node.js](https://nodejs.org/en/)
2. [npm](https://www.npmjs.com/get-npm)
3. [Ruby](https://www.ruby-lang.org/en/)

### Setup
1. Install Sass - `gem install sass`
2. Install grunt-cli globally - `npm install -g grunt-cli`
3. Install protractor globally - `npm install -g protractor`
4. Clone the repository - `git clone https://github.com/mulesoft/api-console.git`
5. Navigate to the directory - `cd api-console`
6. Install the console's NPM packages - `npm install`
7. Install the console's Bower packages - `bower install`

### Running the server
```
$ grunt
```

### Usage
##### Including the console directly
Replace the `<raml-initializer>` directive with `<raml-console-loader>` directive, specifying your RAML as a src attribute in `/dist/index.html`.

##### Including the console via an iframe
```
<iframe src="path/to/dist/index.html?raml=path/to/your.api.raml"/>
```

### HTML Documentation View
##### Overview
![Overview](/screenshots/index-api-console.png)
##### View of Specific Resource
![Overview](/screenshots/resource-view1.png)

![Overview](/screenshots/resource-view2.png)
