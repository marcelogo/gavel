# GAVEL—JavaScript library for HTTP validation

[![Build Status](https://travis-ci.org/apiaryio/gavel.js.png?branch=master)](https://travis-ci.org/apiaryio/gavel.js)
[![Dependency Status](https://david-dm.org/apiaryio/gavel.js.png)](https://david-dm.org/apiaryio/gavel.js)
[![devDependency Status](https://david-dm.org/apiaryio/gavel.js/dev-status.png)](https://david-dm.org/apiaryio/gavel.js#info=devDependencies)
[![Coverage Status](https://coveralls.io/repos/apiaryio/gavel.js/badge.png?branch=coverage)](https://coveralls.io/r/apiaryio/gavel.js?branch=coverage)

## Usage

```
var gavel = require('gavel');
response = {
  "statusCode": "200",
  "headers": {
    "content-type": "application/json",
    "date": "Wed, 03 Jul 2013 13:30:53 GMT",
    "server": "gunicorn/0.17.4",
    "content-length": "30",
    "connection": "keep-alive"
  },
  "body": "{\n  \"origin\": \"94.113.241.2\"\n}"
};
expected = {
  "statusCode": "200",
  "headers": {
    "content-type": "application/json",
    "date": "Wed, 03 Jul 2013 13:30:53 GMT",
    "server": "gunicorn/0.17.4",
    "content-length": "30",
    "connection": "keep-alive"
  },
  "body": "{\n  \"origin\": \"94.113.241.2\"\n}"
};
gavel.isValid(response, expected, 'response', function(error,result){
  console.log result;
});
```

- Find out more on Sync and Async API in [Cucumber documentation and examples](https://www.relishapp.com/apiary/gavel/docs/node-js/)

- Try [command-line interface](https://www.relishapp.com/apiary/gavel/docs/command-line-interface)!

## Installation

```
npm install gavel
```

## Resources

- [Gavel behavior specification](https://www.relishapp.com/apiary/gavel/docs)
- [Github repository](https://github.com/apiaryio/gavel.js)
- [Complete API Reference](http://coffeedoc.info/github/apiaryio/gavel.js/master/)

## Development

```
$ git clone git@github.com:apiaryio/gavel.js.git
$ cd gavel.js
$ git submodule init
$ git submodule update
$ npm install
$ npm test
```

[Codo][codo] API documentation is published with use of [Github post-receive hook](https://help.github.com/articles/post-receive-hooks)

This [README.md][Readme] is generated by build script in [`./scripts/build`] from [Gavel's Cucumber documentation repository][SpecRepo]

[Readme]: https://github.com/apiaryio/gavel.js/blob/master/README.md
[Codo]: https://github.com/netzpirat/codo
[SpecRepo]: https://github.com/apiaryio/gavel/tree/master/node_js



