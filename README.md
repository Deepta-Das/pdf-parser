# @deeptakirandas/pdf-parse

**Javascript cross-platform module to extract texts from PDFs.**

## Installation
`npm i @deeptakirandas/pdf-parse`
 
## Basic Usage - Local Files

```js
const fs = require('fs');
const pdf = require('@deeptakirandas/pdf-parse');

let dataBuffer = fs.readFileSync('path to PDF file...');

pdf(dataBuffer).then(function(data) {

	// number of pages
	console.log(data.numpages);
	// number of rendered pages
	console.log(data.numrender);
	// PDF info
	console.log(data.info);
	// PDF metadata
	console.log(data.metadata); 
	// PDF.js version
	// check https://mozilla.github.io/pdf.js/getting_started/
	console.log(data.version);
	// PDF text
	console.log(data.text); 
        
});
```

## Basic Usage - HTTP
You can use [crawler-request](https://www.npmjs.com/package/crawler-request) which uses the `pdf-parse`

## Exception Handling

```js
const fs = require('fs');
const pdf = require('@deeptakirandas/pdf-parse');

let dataBuffer = fs.readFileSync('path to PDF file...');

pdf(dataBuffer).then(function(data) {
	// use data
})
.catch(function(error){
	// handle exceptions
})
```


## License
[MIT licensed](https://github.com/Deepta-Das/pdf-parser/blob/main/LICENSE) and all it's dependencies are MIT 
