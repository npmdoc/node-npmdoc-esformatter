# api documentation for  [esformatter (v0.10.0)](https://github.com/millermedeiros/esformatter#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-esformatter.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-esformatter) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-esformatter.svg)](https://travis-ci.org/npmdoc/node-npmdoc-esformatter)
#### ECMAScript code beautifier/formatter

[![NPM](https://nodei.co/npm/esformatter.png?downloads=true)](https://www.npmjs.com/package/esformatter)

[![apidoc](https://npmdoc.github.io/node-npmdoc-esformatter/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-esformatter_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-esformatter/build/apidoc.html)

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
            "name": "millermedeiros",
            "email": "miller@millermedeiros.com"
        },
        {
            "name": "jzaefferer",
            "email": "joern.zaefferer@gmail.com"
        }
    ],
    "name": "esformatter",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module esformatter](#apidoc.module.esformatter)
1.  [function <span class="apidocSignatureSpan">esformatter.</span>format (str, opts)](#apidoc.element.esformatter.format)
1.  [function <span class="apidocSignatureSpan">esformatter.</span>rc (filePath, customOptions)](#apidoc.element.esformatter.rc)
1.  [function <span class="apidocSignatureSpan">esformatter.</span>register (plugin)](#apidoc.element.esformatter.register)
1.  [function <span class="apidocSignatureSpan">esformatter.</span>transform (ast, opts)](#apidoc.element.esformatter.transform)
1.  [function <span class="apidocSignatureSpan">esformatter.</span>unregister ()](#apidoc.element.esformatter.unregister)
1.  [function <span class="apidocSignatureSpan">esformatter.</span>unregisterAll ()](#apidoc.element.esformatter.unregisterAll)
1.  object <span class="apidocSignatureSpan">esformatter.</span>diff
1.  object <span class="apidocSignatureSpan">esformatter.</span>helpers
1.  object <span class="apidocSignatureSpan">esformatter.</span>hooks
1.  object <span class="apidocSignatureSpan">esformatter.</span>indent
1.  object <span class="apidocSignatureSpan">esformatter.</span>limit
1.  object <span class="apidocSignatureSpan">esformatter.</span>options
1.  object <span class="apidocSignatureSpan">esformatter.</span>plugins

#### [module esformatter.diff](#apidoc.module.esformatter.diff)
1.  [function <span class="apidocSignatureSpan">esformatter.diff.</span>chars (str, opts, fileName)](#apidoc.element.esformatter.diff.chars)
1.  [function <span class="apidocSignatureSpan">esformatter.diff.</span>unified (str, opts, fileName)](#apidoc.element.esformatter.diff.unified)
1.  [function <span class="apidocSignatureSpan">esformatter.diff.</span>unifiedNoColor (str, opts, fileName)](#apidoc.element.esformatter.diff.unifiedNoColor)

#### [module esformatter.format](#apidoc.module.esformatter.format)
1.  [function <span class="apidocSignatureSpan">esformatter.</span>format (str, opts)](#apidoc.element.esformatter.format.format)
1.  [function <span class="apidocSignatureSpan">esformatter.format.</span>parseFn (str, opts)](#apidoc.element.esformatter.format.parseFn)
1.  object <span class="apidocSignatureSpan">esformatter.format.</span>parseOptions

#### [module esformatter.helpers](#apidoc.module.esformatter.helpers)
1.  [function <span class="apidocSignatureSpan">esformatter.helpers.</span>shouldIndentChild (parent, child, opts)](#apidoc.element.esformatter.helpers.shouldIndentChild)

#### [module esformatter.indent](#apidoc.module.esformatter.indent)
1.  [function <span class="apidocSignatureSpan">esformatter.indent.</span>setOptions (opts)](#apidoc.element.esformatter.indent.setOptions)
1.  [function <span class="apidocSignatureSpan">esformatter.indent.</span>transform (ast)](#apidoc.element.esformatter.indent.transform)

#### [module esformatter.limit](#apidoc.module.esformatter.limit)
1.  [function <span class="apidocSignatureSpan">esformatter.limit.</span>after (token, typeOrValue)](#apidoc.element.esformatter.limit.after)
1.  [function <span class="apidocSignatureSpan">esformatter.limit.</span>around (token, typeOrValue)](#apidoc.element.esformatter.limit.around)
1.  [function <span class="apidocSignatureSpan">esformatter.limit.</span>before (token, typeOrValue)](#apidoc.element.esformatter.limit.before)

#### [module esformatter.options](#apidoc.module.esformatter.options)
1.  [function <span class="apidocSignatureSpan">esformatter.options.</span>get (prop)](#apidoc.element.esformatter.options.get)
1.  [function <span class="apidocSignatureSpan">esformatter.options.</span>getRc (filePath, customOptions)](#apidoc.element.esformatter.options.getRc)
1.  [function <span class="apidocSignatureSpan">esformatter.options.</span>loadAndParseConfig (file)](#apidoc.element.esformatter.options.loadAndParseConfig)
1.  [function <span class="apidocSignatureSpan">esformatter.options.</span>set (opts)](#apidoc.element.esformatter.options.set)
1.  object <span class="apidocSignatureSpan">esformatter.options.</span>presets

#### [module esformatter.plugins](#apidoc.module.esformatter.plugins)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>loadAndRegister (idsOrModules)](#apidoc.element.esformatter.plugins.loadAndRegister)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>nodeAfter ()](#apidoc.element.esformatter.plugins.nodeAfter)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>nodeBefore ()](#apidoc.element.esformatter.plugins.nodeBefore)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>register (plugin)](#apidoc.element.esformatter.plugins.register)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>setOptions (opts)](#apidoc.element.esformatter.plugins.setOptions)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>stringAfter ()](#apidoc.element.esformatter.plugins.stringAfter)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>stringBefore ()](#apidoc.element.esformatter.plugins.stringBefore)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>tokenAfter ()](#apidoc.element.esformatter.plugins.tokenAfter)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>tokenBefore ()](#apidoc.element.esformatter.plugins.tokenBefore)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>transform ()](#apidoc.element.esformatter.plugins.transform)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>transformAfter ()](#apidoc.element.esformatter.plugins.transformAfter)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>transformBefore ()](#apidoc.element.esformatter.plugins.transformBefore)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>unregister ()](#apidoc.element.esformatter.plugins.unregister)
1.  [function <span class="apidocSignatureSpan">esformatter.plugins.</span>unregisterAll ()](#apidoc.element.esformatter.plugins.unregisterAll)



# <a name="apidoc.module.esformatter"></a>[module esformatter](#apidoc.module.esformatter)

#### <a name="apidoc.element.esformatter.format"></a>[function <span class="apidocSignatureSpan">esformatter.</span>format (str, opts)](#apidoc.element.esformatter.format)
- description and source-code
```javascript
function format(str, opts) {
  // we need to load and register the plugins as soon as possible otherwise
  // 'stringBefore' won't be called and default settings won't be used
  _options.set(opts);

  // remove shebang before pipe because piped commands might not know how
  // to handle it
  var prefix = getShebang(str);
  if (prefix && !_options.get('esformatter.allowShebang')) {
    throw new Error(
      'shebang not allowed! Set esformatter.allowShebang to true if you ' +
      'want to support it.'
    );
  }
  str = str.replace(prefix, '');

  var pipeCommands = _options.get('pipe');

  if (pipeCommands) {
    str = pipe(pipeCommands.before, str).toString();
  }

  str = doFormat(str, opts);

  if (pipeCommands) {
    str = pipe(pipeCommands.after, str).toString();
  }

  // we only restore bang after pipe because piped commands might not know how
  // to handle it
  return prefix + str;
}
```
- example usage
```shell
...
  },
  whiteSpace : {
    // ...
  }
};

// return a string with the formatted code
var formattedCode = esformatter.format(codeStr, options);
'''

See the [doc/api.md](./doc/api.md) file for a list of all the public methods
and detailed documentation about each one.

See [doc/config.md](./doc/config.md) for more info about the configuration
options.
...
```

#### <a name="apidoc.element.esformatter.rc"></a>[function <span class="apidocSignatureSpan">esformatter.</span>rc (filePath, customOptions)](#apidoc.element.esformatter.rc)
- description and source-code
```javascript
function getRc(filePath, customOptions) {
  if (isObject(filePath)) {
    customOptions = filePath;
    filePath = null;
  }

  var cwd = process.cwd();

  customOptions = processExtends(cwd, customOptions);

  // if user sets the "preset" we don't load any other config file
  // we assume the "preset" overrides any user settings
  if (isTopLevel(customOptions)) {
    return customOptions;
  }

  // we search for config file starting from source directory or from cwd if
  // path is not provided
  var basedir = filePath ? path.dirname(filePath) : cwd;
  var rc = findAndMergeConfigs(basedir);
  if (isEmpty(rc) && basedir !== cwd) {
    rc = findAndMergeConfigs(cwd);
  }
  var tmpConfig = !isEmpty(rc) ? rc : getGlobalConfig();
  return mergeOptions(tmpConfig, customOptions);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.register"></a>[function <span class="apidocSignatureSpan">esformatter.</span>register (plugin)](#apidoc.element.esformatter.register)
- description and source-code
```javascript
function register(plugin) {
  if (_plugins.indexOf(plugin) === -1) {
    _plugins.push(plugin);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.transform"></a>[function <span class="apidocSignatureSpan">esformatter.</span>transform (ast, opts)](#apidoc.element.esformatter.transform)
- description and source-code
```javascript
function transform(ast, opts) {
  if (opts !== exports.BYPASS_OPTIONS) {
    _options.set(opts);
  }
  // we store this here to avoid calling '_options.get' for each token
  _shouldRemoveTrailingWs = Boolean(_options.get('whiteSpace.removeTrailing'));

  plugins.transformBefore(ast);

  _tk.eachInBetween(ast.startToken, ast.endToken, preprocessToken);
  rocambole.moonwalk(ast, transformNode);
  _tk.eachInBetween(ast.startToken, ast.endToken, postprocessToken);
  _br.limitBeforeEndOfFile(ast);

  // indent should come after all other transformations since it depends on
  // line breaks caused by "parent" nodes, otherwise it will cause conflicts.
  // it should also happen after the postprocessToken since it adds line breaks
  // before/after comments and that changes the indent logic
  indent.transform(ast);

  // plugin transformation comes after the indentation since we assume user
  // knows what he is doing (will increase flexibility and allow plugin to
  // override the indentation logic)
  // we have an alias "transform" to match v0.3 API, but favor 'transformAfter'
  // moving forward. (we might deprecate "transform" in the future)
  plugins.transform(ast);
  plugins.transformAfter(ast);

  return ast;
}
```
- example usage
```shell
...
_tk.eachInBetween(ast.startToken, ast.endToken, postprocessToken);
_br.limitBeforeEndOfFile(ast);

// indent should come after all other transformations since it depends on
// line breaks caused by "parent" nodes, otherwise it will cause conflicts.
// it should also happen after the postprocessToken since it adds line breaks
// before/after comments and that changes the indent logic
indent.transform(ast);

// plugin transformation comes after the indentation since we assume user
// knows what he is doing (will increase flexibility and allow plugin to
// override the indentation logic)
// we have an alias "transform" to match v0.3 API, but favor 'transformAfter'
// moving forward. (we might deprecate "transform" in the future)
plugins.transform(ast);
...
```

#### <a name="apidoc.element.esformatter.unregister"></a>[function <span class="apidocSignatureSpan">esformatter.</span>unregister ()](#apidoc.element.esformatter.unregister)
- description and source-code
```javascript
unregister = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.unregisterAll"></a>[function <span class="apidocSignatureSpan">esformatter.</span>unregisterAll ()](#apidoc.element.esformatter.unregisterAll)
- description and source-code
```javascript
function unregisterAll() {
  _plugins = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.esformatter.diff"></a>[module esformatter.diff](#apidoc.module.esformatter.diff)

#### <a name="apidoc.element.esformatter.diff.chars"></a>[function <span class="apidocSignatureSpan">esformatter.diff.</span>chars (str, opts, fileName)](#apidoc.element.esformatter.diff.chars)
- description and source-code
```javascript
function chars(str, opts, fileName) {
  var result = disparity.chars(str, format(str, opts));
  if (!result) {
    return '';
  }
  // we add a line break at the end because it looks better
  return getHeader(fileName) + result + '\n';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.diff.unified"></a>[function <span class="apidocSignatureSpan">esformatter.diff.</span>unified (str, opts, fileName)](#apidoc.element.esformatter.diff.unified)
- description and source-code
```javascript
function unified(str, opts, fileName) {
  return disparity.unified(str, format(str, opts), {
    paths: [fileName]
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.diff.unifiedNoColor"></a>[function <span class="apidocSignatureSpan">esformatter.diff.</span>unifiedNoColor (str, opts, fileName)](#apidoc.element.esformatter.diff.unifiedNoColor)
- description and source-code
```javascript
function unifiedNoColor(str, opts, fileName) {
  return disparity.unifiedNoColor(str, format(str, opts), {
    paths: [fileName]
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.esformatter.format"></a>[module esformatter.format](#apidoc.module.esformatter.format)

#### <a name="apidoc.element.esformatter.format.format"></a>[function <span class="apidocSignatureSpan">esformatter.</span>format (str, opts)](#apidoc.element.esformatter.format.format)
- description and source-code
```javascript
function format(str, opts) {
  // we need to load and register the plugins as soon as possible otherwise
  // 'stringBefore' won't be called and default settings won't be used
  _options.set(opts);

  // remove shebang before pipe because piped commands might not know how
  // to handle it
  var prefix = getShebang(str);
  if (prefix && !_options.get('esformatter.allowShebang')) {
    throw new Error(
      'shebang not allowed! Set esformatter.allowShebang to true if you ' +
      'want to support it.'
    );
  }
  str = str.replace(prefix, '');

  var pipeCommands = _options.get('pipe');

  if (pipeCommands) {
    str = pipe(pipeCommands.before, str).toString();
  }

  str = doFormat(str, opts);

  if (pipeCommands) {
    str = pipe(pipeCommands.after, str).toString();
  }

  // we only restore bang after pipe because piped commands might not know how
  // to handle it
  return prefix + str;
}
```
- example usage
```shell
...
  },
  whiteSpace : {
    // ...
  }
};

// return a string with the formatted code
var formattedCode = esformatter.format(codeStr, options);
'''

See the [doc/api.md](./doc/api.md) file for a list of all the public methods
and detailed documentation about each one.

See [doc/config.md](./doc/config.md) for more info about the configuration
options.
...
```

#### <a name="apidoc.element.esformatter.format.parseFn"></a>[function <span class="apidocSignatureSpan">esformatter.format.</span>parseFn (str, opts)](#apidoc.element.esformatter.format.parseFn)
- description and source-code
```javascript
parseFn = function (str, opts) {
  return parser.parse(str, opts);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.esformatter.helpers"></a>[module esformatter.helpers](#apidoc.module.esformatter.helpers)

#### <a name="apidoc.element.esformatter.helpers.shouldIndentChild"></a>[function <span class="apidocSignatureSpan">esformatter.helpers.</span>shouldIndentChild (parent, child, opts)](#apidoc.element.esformatter.helpers.shouldIndentChild)
- description and source-code
```javascript
function shouldIndentChild(parent, child, opts) {
  // this will avoid indenting objects/arrays/functions twice if they
  // are on the right of a BinaryExpression, LogicalExpression or
  // UnaryExpression
  if (!child || !opts[parent.type + '.' + child.type]) {
    return false;
  }

  return !child.right || !opts[child.right.type];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.esformatter.indent"></a>[module esformatter.indent](#apidoc.module.esformatter.indent)

#### <a name="apidoc.element.esformatter.indent.setOptions"></a>[function <span class="apidocSignatureSpan">esformatter.indent.</span>setOptions (opts)](#apidoc.element.esformatter.indent.setOptions)
- description and source-code
```javascript
function setOptions(opts) {
  _opts = opts;
  indent.setOptions(opts);
}
```
- example usage
```shell
...

// ---


exports.setOptions = setOptions;
function setOptions(opts) {
_opts = opts;
indent.setOptions(opts);
}


// transform AST in place
exports.transform = transform;
function transform(ast) {
rocambole.walk(ast, transformNode);
...
```

#### <a name="apidoc.element.esformatter.indent.transform"></a>[function <span class="apidocSignatureSpan">esformatter.indent.</span>transform (ast)](#apidoc.element.esformatter.indent.transform)
- description and source-code
```javascript
function transform(ast) {
  rocambole.walk(ast, transformNode);
  indent.sanitize(ast);
  // on v0.6.0 we named the property starting with uppercase "A" by mistake, so
  // now we need to support both styles to keep consistency :(
  if (_opts.alignComments) {
    indent.alignComments(ast);
  }
  return ast;
}
```
- example usage
```shell
...
_tk.eachInBetween(ast.startToken, ast.endToken, postprocessToken);
_br.limitBeforeEndOfFile(ast);

// indent should come after all other transformations since it depends on
// line breaks caused by "parent" nodes, otherwise it will cause conflicts.
// it should also happen after the postprocessToken since it adds line breaks
// before/after comments and that changes the indent logic
indent.transform(ast);

// plugin transformation comes after the indentation since we assume user
// knows what he is doing (will increase flexibility and allow plugin to
// override the indentation logic)
// we have an alias "transform" to match v0.3 API, but favor 'transformAfter'
// moving forward. (we might deprecate "transform" in the future)
plugins.transform(ast);
...
```



# <a name="apidoc.module.esformatter.limit"></a>[module esformatter.limit](#apidoc.module.esformatter.limit)

#### <a name="apidoc.element.esformatter.limit.after"></a>[function <span class="apidocSignatureSpan">esformatter.limit.</span>after (token, typeOrValue)](#apidoc.element.esformatter.limit.after)
- description and source-code
```javascript
function limitAfter(token, typeOrValue) {
  _br.limitAfter(token, typeOrValue);
  _ws.limitAfter(token, typeOrValue);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.limit.around"></a>[function <span class="apidocSignatureSpan">esformatter.limit.</span>around (token, typeOrValue)](#apidoc.element.esformatter.limit.around)
- description and source-code
```javascript
function limitAround(token, typeOrValue) {
  _br.limit(token, typeOrValue);
  _ws.limit(token, typeOrValue);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.limit.before"></a>[function <span class="apidocSignatureSpan">esformatter.limit.</span>before (token, typeOrValue)](#apidoc.element.esformatter.limit.before)
- description and source-code
```javascript
function limitBefore(token, typeOrValue) {
  _br.limitBefore(token, typeOrValue);
  _ws.limitBefore(token, typeOrValue);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.esformatter.options"></a>[module esformatter.options](#apidoc.module.esformatter.options)

#### <a name="apidoc.element.esformatter.options.get"></a>[function <span class="apidocSignatureSpan">esformatter.options.</span>get (prop)](#apidoc.element.esformatter.options.get)
- description and source-code
```javascript
get = function (prop) {
  return prop ? get(_curOpts, prop) : _curOpts;
}
```
- example usage
```shell
...
// ---

function transform(ast, opts) {
if (opts !== exports.BYPASS_OPTIONS) {
  _options.set(opts);
}
// we store this here to avoid calling '_options.get' for each token
_shouldRemoveTrailingWs = Boolean(_options.get('whiteSpace.removeTrailing'));

plugins.transformBefore(ast);

_tk.eachInBetween(ast.startToken, ast.endToken, preprocessToken);
rocambole.moonwalk(ast, transformNode);
_tk.eachInBetween(ast.startToken, ast.endToken, postprocessToken);
_br.limitBeforeEndOfFile(ast);
...
```

#### <a name="apidoc.element.esformatter.options.getRc"></a>[function <span class="apidocSignatureSpan">esformatter.options.</span>getRc (filePath, customOptions)](#apidoc.element.esformatter.options.getRc)
- description and source-code
```javascript
function getRc(filePath, customOptions) {
  if (isObject(filePath)) {
    customOptions = filePath;
    filePath = null;
  }

  var cwd = process.cwd();

  customOptions = processExtends(cwd, customOptions);

  // if user sets the "preset" we don't load any other config file
  // we assume the "preset" overrides any user settings
  if (isTopLevel(customOptions)) {
    return customOptions;
  }

  // we search for config file starting from source directory or from cwd if
  // path is not provided
  var basedir = filePath ? path.dirname(filePath) : cwd;
  var rc = findAndMergeConfigs(basedir);
  if (isEmpty(rc) && basedir !== cwd) {
    rc = findAndMergeConfigs(cwd);
  }
  var tmpConfig = !isEmpty(rc) ? rc : getGlobalConfig();
  return mergeOptions(tmpConfig, customOptions);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.options.loadAndParseConfig"></a>[function <span class="apidocSignatureSpan">esformatter.options.</span>loadAndParseConfig (file)](#apidoc.element.esformatter.options.loadAndParseConfig)
- description and source-code
```javascript
function loadAndParseConfig(file) {
  try {
    var config = JSON.parse(
      stripJsonComments(fs.readFileSync(file).toString())
    );

    return processExtends(path.dirname(file), config);
  } catch (e) {
    // include file name and let user know error was caused by config file
    // parsing. this is redundant for ENOENT errors but very helpful for
    // JSON.parse
    throw new Error(
      "Can't parse configuration file '" + file + "'. Exception: " + e.message
    );
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.options.set"></a>[function <span class="apidocSignatureSpan">esformatter.options.</span>set (opts)](#apidoc.element.esformatter.options.set)
- description and source-code
```javascript
set = function (opts) {
  var preset = opts && opts.preset ? opts.preset : 'default';
  // we need to pass all the user settings and default settings to the plugins
  // so they are able to toggle the behavior and make changes based on the
  // options
  _curOpts = mergePreset(preset, opts);

  // FIXME: deprecate AlignComments on v1.0
  // on v0.6.0 we named the property starting with uppercase "A" by mistake, so
  // now we need to support both styles to keep consistency :(
  if (_curOpts.indent && 'AlignComments' in _curOpts.indent) {
    _curOpts.indent.alignComments = _curOpts.indent.AlignComments;
  }

  _ws.setOptions(_curOpts.whiteSpace);
  _br.setOptions(_curOpts.lineBreak);
  indent.setOptions(_curOpts.indent);
  plugins.setOptions(_curOpts);

  // user provided options should override default settings and also any
  // changes made by plugins
  if (opts) {
    _curOpts = deepMixIn(_curOpts, opts);
  }
}
```
- example usage
```shell
...
// from inside 'format'
exports.BYPASS_OPTIONS = {};

// ---

function transform(ast, opts) {
if (opts !== exports.BYPASS_OPTIONS) {
  _options.set(opts);
}
// we store this here to avoid calling '_options.get' for each token
_shouldRemoveTrailingWs = Boolean(_options.get('whiteSpace.removeTrailing'));

plugins.transformBefore(ast);

_tk.eachInBetween(ast.startToken, ast.endToken, preprocessToken);
...
```



# <a name="apidoc.module.esformatter.plugins"></a>[module esformatter.plugins](#apidoc.module.esformatter.plugins)

#### <a name="apidoc.element.esformatter.plugins.loadAndRegister"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>loadAndRegister (idsOrModules)](#apidoc.element.esformatter.plugins.loadAndRegister)
- description and source-code
```javascript
function loadAndRegister(idsOrModules) {
  idsOrModules = idsOrModules || [];
  idsOrModules.forEach(function(idOrModule) {
    var module = isObject(idOrModule) ?
      idOrModule :
      loadModule(idOrModule);
    register(module);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.plugins.nodeAfter"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>nodeAfter ()](#apidoc.element.esformatter.plugins.nodeAfter)
- description and source-code
```javascript
nodeAfter = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
...
  _ws.limitBefore(node.startToken, node.type);
  _ws.limitAfter(node.endToken, node.type);
}

// handle parenthesis automatically since it is needed by multiple node types
// and it avoids code duplication and reduces complexity of each hook
expressionParentheses.addSpaceInside(node);
plugins.nodeAfter(node);
}


function preprocessToken(token) {
if (_tk.isComment(token)) {
  _br.limit(token, token.type);
}
...
```

#### <a name="apidoc.element.esformatter.plugins.nodeBefore"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>nodeBefore ()](#apidoc.element.esformatter.plugins.nodeBefore)
- description and source-code
```javascript
nodeBefore = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
...
plugins.transformAfter(ast);

return ast;
}


function transformNode(node) {
plugins.nodeBefore(node);
addBrAroundNode(node);

var hook = hooks[node.type];
if (hook && 'format' in hook) {
  hook.format(node);
}
...
```

#### <a name="apidoc.element.esformatter.plugins.register"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>register (plugin)](#apidoc.element.esformatter.plugins.register)
- description and source-code
```javascript
function register(plugin) {
  if (_plugins.indexOf(plugin) === -1) {
    _plugins.push(plugin);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.plugins.setOptions"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>setOptions (opts)](#apidoc.element.esformatter.plugins.setOptions)
- description and source-code
```javascript
setOptions = function (opts) {
  loadAndRegister(opts && opts.plugins);
  // esformatter ends up being a circular dependency,
  // but this was the quickest way of doing it :P
  // needed specially because of issue #348
  exec('setOptions', opts, require('./esformatter'));
}
```
- example usage
```shell
...

// ---


exports.setOptions = setOptions;
function setOptions(opts) {
_opts = opts;
indent.setOptions(opts);
}


// transform AST in place
exports.transform = transform;
function transform(ast) {
rocambole.walk(ast, transformNode);
...
```

#### <a name="apidoc.element.esformatter.plugins.stringAfter"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>stringAfter ()](#apidoc.element.esformatter.plugins.stringAfter)
- description and source-code
```javascript
stringAfter = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.plugins.stringBefore"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>stringBefore ()](#apidoc.element.esformatter.plugins.stringBefore)
- description and source-code
```javascript
stringBefore = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.plugins.tokenAfter"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>tokenAfter ()](#apidoc.element.esformatter.plugins.tokenAfter)
- description and source-code
```javascript
tokenAfter = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
...

function postprocessToken(token) {
if (_tk.isComment(token)) {
  processComment(token);
} else if (_shouldRemoveTrailingWs && _tk.isWs(token)) {
  removeTrailingWs(token);
}
plugins.tokenAfter(token);
}


function processComment(token) {
_ws.limitBefore(token, token.type);
// only block comment needs space afterwards
if (token.type === 'BlockComment') {
...
```

#### <a name="apidoc.element.esformatter.plugins.tokenBefore"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>tokenBefore ()](#apidoc.element.esformatter.plugins.tokenBefore)
- description and source-code
```javascript
tokenBefore = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
...
}


function preprocessToken(token) {
if (_tk.isComment(token)) {
  _br.limit(token, token.type);
}
plugins.tokenBefore(token);
}


function postprocessToken(token) {
if (_tk.isComment(token)) {
  processComment(token);
} else if (_shouldRemoveTrailingWs && _tk.isWs(token)) {
...
```

#### <a name="apidoc.element.esformatter.plugins.transform"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>transform ()](#apidoc.element.esformatter.plugins.transform)
- description and source-code
```javascript
transform = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
...
_tk.eachInBetween(ast.startToken, ast.endToken, postprocessToken);
_br.limitBeforeEndOfFile(ast);

// indent should come after all other transformations since it depends on
// line breaks caused by "parent" nodes, otherwise it will cause conflicts.
// it should also happen after the postprocessToken since it adds line breaks
// before/after comments and that changes the indent logic
indent.transform(ast);

// plugin transformation comes after the indentation since we assume user
// knows what he is doing (will increase flexibility and allow plugin to
// override the indentation logic)
// we have an alias "transform" to match v0.3 API, but favor 'transformAfter'
// moving forward. (we might deprecate "transform" in the future)
plugins.transform(ast);
...
```

#### <a name="apidoc.element.esformatter.plugins.transformAfter"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>transformAfter ()](#apidoc.element.esformatter.plugins.transformAfter)
- description and source-code
```javascript
transformAfter = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
...

// plugin transformation comes after the indentation since we assume user
// knows what he is doing (will increase flexibility and allow plugin to
// override the indentation logic)
// we have an alias "transform" to match v0.3 API, but favor 'transformAfter'
// moving forward. (we might deprecate "transform" in the future)
plugins.transform(ast);
plugins.transformAfter(ast);

return ast;
}


function transformNode(node) {
plugins.nodeBefore(node);
...
```

#### <a name="apidoc.element.esformatter.plugins.transformBefore"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>transformBefore ()](#apidoc.element.esformatter.plugins.transformBefore)
- description and source-code
```javascript
transformBefore = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
...
function transform(ast, opts) {
if (opts !== exports.BYPASS_OPTIONS) {
  _options.set(opts);
}
// we store this here to avoid calling '_options.get' for each token
_shouldRemoveTrailingWs = Boolean(_options.get('whiteSpace.removeTrailing'));

plugins.transformBefore(ast);

_tk.eachInBetween(ast.startToken, ast.endToken, preprocessToken);
rocambole.moonwalk(ast, transformNode);
_tk.eachInBetween(ast.startToken, ast.endToken, postprocessToken);
_br.limitBeforeEndOfFile(ast);

// indent should come after all other transformations since it depends on
...
```

#### <a name="apidoc.element.esformatter.plugins.unregister"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>unregister ()](#apidoc.element.esformatter.plugins.unregister)
- description and source-code
```javascript
unregister = function () {
    var rest = slice(arguments);

    // Don't waste time checking for placeholders if there aren't any.
    var args = has_ ? take(as.length, function(i) {
        var a = as[i];
        return a === _ ? rest.shift() : a;
    }) : as;

    return f.apply(this, rest.length ? args.concat(rest) : args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.esformatter.plugins.unregisterAll"></a>[function <span class="apidocSignatureSpan">esformatter.plugins.</span>unregisterAll ()](#apidoc.element.esformatter.plugins.unregisterAll)
- description and source-code
```javascript
function unregisterAll() {
  _plugins = [];
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
