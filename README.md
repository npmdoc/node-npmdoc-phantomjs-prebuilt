# api documentation for  [phantomjs-prebuilt (v2.1.14)](https://github.com/Medium/phantomjs)  [![npm package](https://img.shields.io/npm/v/npmdoc-phantomjs-prebuilt.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-phantomjs-prebuilt) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-phantomjs-prebuilt.svg)](https://travis-ci.org/npmdoc/node-npmdoc-phantomjs-prebuilt)
#### Headless WebKit with JS API

[![NPM](https://nodei.co/npm/phantomjs-prebuilt.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/phantomjs-prebuilt)

[![apidoc](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Pupius",
        "url": "http://pupius.co.uk"
    },
    "bin": {
        "phantomjs": "./bin/phantomjs"
    },
    "bugs": {
        "url": "https://github.com/Medium/phantomjs/issues"
    },
    "dependencies": {
        "es6-promise": "~4.0.3",
        "extract-zip": "~1.5.0",
        "fs-extra": "~1.0.0",
        "hasha": "~2.2.0",
        "kew": "~0.7.0",
        "progress": "~1.1.8",
        "request": "~2.79.0",
        "request-progress": "~2.0.1",
        "which": "~1.2.10"
    },
    "description": "Headless WebKit with JS API",
    "devDependencies": {
        "eslint": "2.7.0",
        "nodeunit": "0.9.1",
        "webdriverio": "~4.2.3"
    },
    "directories": {},
    "dist": {
        "shasum": "d53d311fcfb7d1d08ddb24014558f1188c516da0",
        "tarball": "https://registry.npmjs.org/phantomjs-prebuilt/-/phantomjs-prebuilt-2.1.14.tgz"
    },
    "gitHead": "750d5f32e1586fe0b34c782dd87f60cbb21e6441",
    "homepage": "https://github.com/Medium/phantomjs",
    "keywords": [
        "phantomjs",
        "headless",
        "webkit"
    ],
    "license": "Apache-2.0",
    "main": "lib/phantomjs",
    "maintainers": [
        {
            "name": "dpup"
        },
        {
            "name": "medium"
        },
        {
            "name": "nicks"
        }
    ],
    "name": "phantomjs-prebuilt",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/Medium/phantomjs.git"
    },
    "scripts": {
        "install": "node install.js",
        "test": "nodeunit --reporter=minimal test/tests.js && eslint ."
    },
    "version": "2.1.14"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module phantomjs-prebuilt](#apidoc.module.phantomjs-prebuilt)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>cleanPath (path)](#apidoc.element.phantomjs-prebuilt.cleanPath)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>exec ()](#apidoc.element.phantomjs-prebuilt.exec)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>run ()](#apidoc.element.phantomjs-prebuilt.run)
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>arch
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>path
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>platform
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>version



# <a name="apidoc.module.phantomjs-prebuilt"></a>[module phantomjs-prebuilt](#apidoc.module.phantomjs-prebuilt)

#### <a name="apidoc.element.phantomjs-prebuilt.cleanPath"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>cleanPath (path)](#apidoc.element.phantomjs-prebuilt.cleanPath)
- description and source-code
```javascript
cleanPath = function (path) {
  return path
      .replace(/:[^:]*node_modules[^:]*/g, '')
      .replace(/(^|:)\.\/bin(\:|$)/g, ':')
      .replace(/^:+/, '')
      .replace(/:+$/, '')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.phantomjs-prebuilt.exec"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>exec ()](#apidoc.element.phantomjs-prebuilt.exec)
- description and source-code
```javascript
exec = function () {
  var args = Array.prototype.slice.call(arguments)
  return spawn(exports.path, args)
}
```
- example usage
```shell
...

'''

Or 'exec()' method is also provided for convenience:

'''javascript
var phantomjs = require('phantomjs-prebuilt')
var program = phantomjs.exec('phantomjs-script.js', 'arg1', 'arg2')
program.stdout.pipe(process.stdout)
program.stderr.pipe(process.stderr)
program.on('exit', code => {
  // do something on end
})
'''
...
```

#### <a name="apidoc.element.phantomjs-prebuilt.run"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>run ()](#apidoc.element.phantomjs-prebuilt.run)
- description and source-code
```javascript
run = function () {
  var args = arguments
  return new Promise(function (resolve, reject) {
    try {
      var program = exports.exec.apply(null, args)
      var isFirst = true
      var stderr = ''
      program.stdout.on('data', function () {
        // This detects PhantomJS instance get ready.
        if (!isFirst) return
        isFirst = false
        resolve(program)
      })
      program.stderr.on('data', function (data) {
        stderr = stderr + data.toString('utf8')
      })
      program.on('error', function (err) {
        if (!isFirst) return
        isFirst = false
        reject(err)
      })
      program.on('exit', function (code) {
        if (!isFirst) return
        isFirst = false
        if (code == 0) {
          // PhantomJS doesn't use exit codes correctly :(
          if (stderr.indexOf('Error:') == 0) {
            reject(new Error(stderr))
          } else {
            resolve(program)
          }
        } else {
          reject(new Error('Exit code: ' + code))
        }
      })
    } catch (err) {
      reject(err)
    }
  })
}
```
- example usage
```shell
...
'run()' method detects when PhantomJS gets ready. It's handy to use with WebDriver (Selenium).

'''javascript
var phantomjs = require('phantomjs-prebuilt')
var webdriverio = require('webdriverio')
var wdOpts = { desiredCapabilities: { browserName: 'phantomjs' } }

phantomjs.run('--webdriver=4444').then(program => {
  webdriverio.remote(wdOpts).init()
    .url('https://developer.mozilla.org/en-US/')
    .getTitle().then(title => {
      console.log(title) // 'Mozilla Developer Network'
      program.kill() // quits PhantomJS
    })
})
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
