# npmdoc-esformatter

#### api documentation for  [esformatter (v0.10.0)](https://github.com/millermedeiros/esformatter#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-esformatter.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-esformatter) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-esformatter.svg)](https://travis-ci.org/npmdoc/node-npmdoc-esformatter)

#### ECMAScript code beautifier/formatter

[![NPM](https://nodei.co/npm/esformatter.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/esformatter)

- [https://npmdoc.github.io/node-npmdoc-esformatter/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-esformatter/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-esformatter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-esformatter/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-esformatter/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-esformatter/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Miller Medeiros",
        "url": "http://blog.millermedeiros.com/"
    },
    "bin": {
        "esformatter": "./bin/esformatter"
    },
    "bugs": {
        "url": "https://github.com/millermedeiros/esformatter/issues"
    },
    "dependencies": {
        "acorn-to-esprima": "^2.0.6",
        "babel-traverse": "^6.4.5",
        "debug": "^0.7.4",
        "disparity": "^2.0.0",
        "esformatter-parser": "^1.0.0",
        "glob": "^7.0.5",
        "minimatch": "^3.0.2",
        "minimist": "^1.1.1",
        "mout": ">=0.9 <2.0",
        "npm-run": "^3.0.0",
        "resolve": "^1.1.5",
        "rocambole": ">=0.7 <2.0",
        "rocambole-indent": "^2.0.4",
        "rocambole-linebreak": "^1.0.2",
        "rocambole-node": "~1.0",
        "rocambole-token": "^1.1.2",
        "rocambole-whitespace": "^1.0.0",
        "stdin": "*",
        "strip-json-comments": "~0.1.1",
        "supports-color": "^1.3.1",
        "user-home": "^2.0.0"
    },
    "description": "ECMAScript code beautifier/formatter",
    "devDependencies": {
        "chai": "1.4",
        "esformatter-pipe-test": "file:test/pipe",
        "esformatter-preset-fake-1": "file:test/preset/fake1",
        "esformatter-preset-fake-2": "file:test/preset/fake2",
        "esformatter-test-plugin": "file:test/plugin",
        "jshint": "~2.3.0",
        "mocha": "https://github.com/millermedeiros/mocha/tarball/latest",
        "mockery": "^1.4.0"
    },
    "directories": {
        "doc": "./doc",
        "bin": "./bin",
        "lib": "./lib"
    },
    "dist": {
        "shasum": "e321ecc3d94083372cdfcf5c6f942cef6fec59d3",
        "tarball": "https://registry.npmjs.org/esformatter/-/esformatter-0.10.0.tgz"
    },
    "esformatter": {
        "root": true
    },
    "gitHead": "2198969924e9c461a02fc635cc7a5fcf5f31afe9",
    "homepage": "https://github.com/millermedeiros/esformatter#readme",
    "keywords": [
        "babel",
        "beautifier",
        "beautify",
        "ecmascript",
        "esprima",
        "format",
        "formatter",
        "javascript",
        "jscs",
        "source",
        "style",
        "syntax"
    ],
    "license": "MIT",
    "main": "lib/esformatter.js",
    "maintainers": [
        {
            "name": "millermedeiros"
        },
        {
            "name": "jzaefferer"
        }
    ],
    "name": "esformatter",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/millermedeiros/esformatter.git"
    },
    "scripts": {
        "format": "esformatter -i 'lib/**/*.js' 'test/*.js'",
        "lint": "jshint lib/*.js lib/**/*.js test/*.js && ./bin/esformatter --diff 'lib/**/*.js' 'test/*.js'",
        "test": "node test/runner.js"
    },
    "version": "0.10.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
