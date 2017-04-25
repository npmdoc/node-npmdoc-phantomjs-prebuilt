# npmdoc-phantomjs-prebuilt

#### basic api documentation for  [phantomjs-prebuilt (v2.1.14)](https://github.com/Medium/phantomjs)  [![npm package](https://img.shields.io/npm/v/npmdoc-phantomjs-prebuilt.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-phantomjs-prebuilt) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-phantomjs-prebuilt.svg)](https://travis-ci.org/npmdoc/node-npmdoc-phantomjs-prebuilt)

#### Headless WebKit with JS API

[![NPM](https://nodei.co/npm/phantomjs-prebuilt.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/phantomjs-prebuilt)

- [https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-phantomjs-prebuilt/build/apidoc.html)

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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
