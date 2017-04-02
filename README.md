# api documentation for  [phantomjs-prebuilt (v2.1.14)](https://github.com/Medium/phantomjs)  [![npm package](https://img.shields.io/npm/v/npmdoc-phantomjs-prebuilt.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-phantomjs-prebuilt) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-phantomjs-prebuilt.svg)](https://travis-ci.org/npmdoc/node-npmdoc-phantomjs-prebuilt)
#### Headless WebKit with JS API

[![NPM](https://nodei.co/npm/phantomjs-prebuilt.png?downloads=true)](https://www.npmjs.com/package/phantomjs-prebuilt)

[![apidoc](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-phantomjs-prebuilt_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Pupius",
        "email": "dan@obvious.com",
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
            "name": "dpup",
            "email": "dan@pupi.us"
        },
        {
            "name": "medium",
            "email": "npm@medium.com"
        },
        {
            "name": "nicks",
            "email": "nicholas.j.santos+npm@gmail.com"
        }
    ],
    "name": "phantomjs-prebuilt",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
1.  object <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>util
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>arch
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>path
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>platform
1.  string <span class="apidocSignatureSpan">phantomjs-prebuilt.</span>version

#### [module phantomjs-prebuilt.util](#apidoc.module.phantomjs-prebuilt.util)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>checkPhantomjsVersion (phantomPath)](#apidoc.element.phantomjs-prebuilt.util.checkPhantomjsVersion)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>findValidPhantomJsBinary (libPath)](#apidoc.element.phantomjs-prebuilt.util.findValidPhantomJsBinary)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>getDownloadSpec ()](#apidoc.element.phantomjs-prebuilt.util.getDownloadSpec)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>getTargetArch ()](#apidoc.element.phantomjs-prebuilt.util.getTargetArch)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>getTargetPlatform ()](#apidoc.element.phantomjs-prebuilt.util.getTargetPlatform)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>verifyChecksum (fileName, checksum)](#apidoc.element.phantomjs-prebuilt.util.verifyChecksum)
1.  [function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>writeLocationFile (location)](#apidoc.element.phantomjs-prebuilt.util.writeLocationFile)



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
...
    exit(1)
  }
})

// NPM adds bin directories to the path, which will cause 'which' to find the
// bin for this package not the actual phantomjs bin.  Also help out people who
// put ./bin on their path
process.env.PATH = helper.cleanPath(originalPath)

var libPath = path.join(__dirname, 'lib')
var pkgPath = path.join(libPath, 'phantom')
var phantomPath = null

// If the user manually installed PhantomJS, we want
// to use the existing version.
...
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



# <a name="apidoc.module.phantomjs-prebuilt.util"></a>[module phantomjs-prebuilt.util](#apidoc.module.phantomjs-prebuilt.util)

#### <a name="apidoc.element.phantomjs-prebuilt.util.checkPhantomjsVersion"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>checkPhantomjsVersion (phantomPath)](#apidoc.element.phantomjs-prebuilt.util.checkPhantomjsVersion)
- description and source-code
```javascript
function checkPhantomjsVersion(phantomPath) {
  console.log('Found PhantomJS at', phantomPath, '...verifying')
  return kew.nfcall(cp.execFile, phantomPath, ['--version']).then(function (stdout) {
    var version = stdout.trim()
    if (helper.version == version) {
      return true
    } else {
      console.log('PhantomJS detected, but wrong version', stdout.trim(), '@', phantomPath + '.')
      return false
    }
  }).fail(function (err) {
    console.error('Error verifying phantomjs, continuing', err)
    return false
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.phantomjs-prebuilt.util.findValidPhantomJsBinary"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>findValidPhantomJsBinary (libPath)](#apidoc.element.phantomjs-prebuilt.util.findValidPhantomJsBinary)
- description and source-code
```javascript
function findValidPhantomJsBinary(libPath) {
  return kew.fcall(function () {
    var libModule = require(libPath)
    if (libModule.location &&
        getTargetPlatform() == libModule.platform &&
        getTargetArch() == libModule.arch) {
      var resolvedLocation = path.resolve(path.dirname(libPath), libModule.location)
      if (fs.statSync(resolvedLocation)) {
        return checkPhantomjsVersion(resolvedLocation).then(function (matches) {
          if (matches) {
            return kew.resolve(resolvedLocation)
          }
        })
      }
    }
    return false
  }).fail(function () {
    return false
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.phantomjs-prebuilt.util.getDownloadSpec"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>getDownloadSpec ()](#apidoc.element.phantomjs-prebuilt.util.getDownloadSpec)
- description and source-code
```javascript
function getDownloadSpec() {
  var cdnUrl = process.env.npm_config_phantomjs_cdnurl ||
      process.env.PHANTOMJS_CDNURL ||
      DEFAULT_CDN
  var downloadUrl = cdnUrl + '/phantomjs-' + helper.version + '-'
  var checksum = ''

  var platform = getTargetPlatform()
  var arch = getTargetArch()
  if (platform === 'linux' && arch === 'x64') {
    downloadUrl += 'linux-x86_64.tar.bz2'
    checksum = '86dd9a4bf4aee45f1a84c9f61cf1947c1d6dce9b9e8d2a907105da7852460d2f'
  } else if (platform === 'linux' && arch == 'ia32') {
    downloadUrl += 'linux-i686.tar.bz2'
    checksum = '80e03cfeb22cc4dfe4e73b68ab81c9fdd7c78968cfd5358e6af33960464f15e3'
  } else if (platform === 'darwin') {
    downloadUrl += 'macosx.zip'
    checksum = '538cf488219ab27e309eafc629e2bcee9976990fe90b1ec334f541779150f8c1'
  } else if (platform === 'win32') {
    downloadUrl += 'windows.zip'
    checksum = 'd9fb05623d6b26d3654d008eab3adafd1f6350433dfd16138c46161f42c7dcc8'
  } else {
    return null
  }
  return {url: downloadUrl, checksum: checksum}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.phantomjs-prebuilt.util.getTargetArch"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>getTargetArch ()](#apidoc.element.phantomjs-prebuilt.util.getTargetArch)
- description and source-code
```javascript
function getTargetArch() {
  return process.env.PHANTOMJS_ARCH || process.arch
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.phantomjs-prebuilt.util.getTargetPlatform"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>getTargetPlatform ()](#apidoc.element.phantomjs-prebuilt.util.getTargetPlatform)
- description and source-code
```javascript
function getTargetPlatform() {
  return process.env.PHANTOMJS_PLATFORM || process.platform
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.phantomjs-prebuilt.util.verifyChecksum"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>verifyChecksum (fileName, checksum)](#apidoc.element.phantomjs-prebuilt.util.verifyChecksum)
- description and source-code
```javascript
function verifyChecksum(fileName, checksum) {
  return kew.resolve(hasha.fromFile(fileName, {algorithm: 'sha256'})).then(function (hash) {
    var result = checksum == hash
    if (result) {
      console.log('Verified checksum of previously downloaded file')
    } else {
      console.log('Checksum did not match')
    }
    return result
  }).fail(function (err) {
    console.error('Failed to verify checksum: ', err)
    return false
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.phantomjs-prebuilt.util.writeLocationFile"></a>[function <span class="apidocSignatureSpan">phantomjs-prebuilt.util.</span>writeLocationFile (location)](#apidoc.element.phantomjs-prebuilt.util.writeLocationFile)
- description and source-code
```javascript
function writeLocationFile(location) {
  console.log('Writing location.js file')
  if (getTargetPlatform() === 'win32') {
    location = location.replace(/\\/g, '\\\\')
  }

  var platform = getTargetPlatform()
  var arch = getTargetArch()

  var contents = 'module.exports.location = "' + location + '"\n'

  if (/^[a-zA-Z0-9]*$/.test(platform) && /^[a-zA-Z0-9]*$/.test(arch)) {
    contents +=
        'module.exports.platform = "' + getTargetPlatform() + '"\n' +
        'module.exports.arch = "' + getTargetArch() + '"\n'
  }

  fs.writeFileSync(path.join(libPath, 'location.js'), contents)
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
