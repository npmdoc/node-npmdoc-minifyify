# npmdoc-minifyify

#### api documentation for  [minifyify (v7.3.5)](https://github.com/ben-ng/minifyify#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-minifyify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-minifyify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-minifyify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-minifyify)

#### Minify your browserify bundles without losing the sourcemap

[![NPM](https://nodei.co/npm/minifyify.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/minifyify)

- [https://npmdoc.github.io/node-npmdoc-minifyify/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-minifyify/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-minifyify/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-minifyify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-minifyify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-minifyify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ben Ng",
        "url": "http://benng.me"
    },
    "bugs": {
        "url": "https://github.com/ben-ng/minifyify/issues"
    },
    "contributors": [
        {
            "name": "Jesús Leganés Combarro 'piranna'",
            "url": "http://pirannafs.blogspot.com.es"
        }
    ],
    "dependencies": {
        "concat-stream": "^1.4.7",
        "convert-source-map": "^1.0.0",
        "lodash.assign": "^4.0.0",
        "lodash.bind": "^4.0.0",
        "lodash.defaults": "^4.0.0",
        "lodash.foreach": "^4.0.0",
        "mkdirp": "^0.5.0",
        "source-map": "^0.5.3",
        "through": "^2.3.6",
        "tmp": "0.0.28",
        "transform-filter": "^0.1.1",
        "uglify-js": "^2.6.1"
    },
    "description": "Minify your browserify bundles without losing the sourcemap",
    "devDependencies": {
        "backbone": "latest",
        "brfs": "latest",
        "browserify": "latest",
        "coffeeify": "latest",
        "envify": "latest",
        "handlebars": "latest",
        "handlebars-runtime": "latest",
        "hbsfy": "latest",
        "jake": "latest",
        "jquery": "latest",
        "jquery-browserify": "latest",
        "jsesc": "latest",
        "lodash.template": "latest",
        "sourcemap-validator": "latest",
        "test-peer-range": "^1.0.1",
        "utilities": "latest"
    },
    "directories": {},
    "dist": {
        "shasum": "9f4bb0c8692502478d8ee85b10bd7248570629ae",
        "tarball": "https://registry.npmjs.org/minifyify/-/minifyify-7.3.5.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "86a9cbd2d177ca76be42c956d43899945f2909de",
    "homepage": "https://github.com/ben-ng/minifyify#readme",
    "keywords": [
        "browserify-plugin",
        "browserify",
        "uglify",
        "transform",
        "minify",
        "uglifyify",
        "compress"
    ],
    "license": "MIT",
    "main": "./lib",
    "maintainers": [
        {
            "name": "benng"
        }
    ],
    "name": "minifyify",
    "optionalDependencies": {},
    "peerDependencies": {
        "browserify": ">= 5"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/ben-ng/minifyify.git"
    },
    "scripts": {
        "test": "test-peer-range browserify",
        "test-main": "jake test --trace"
    },
    "version": "7.3.5"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
