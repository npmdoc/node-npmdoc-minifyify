# api documentation for  [minifyify (v7.3.5)](https://github.com/ben-ng/minifyify#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-minifyify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-minifyify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-minifyify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-minifyify)
#### Minify your browserify bundles without losing the sourcemap

[![NPM](https://nodei.co/npm/minifyify.png?downloads=true)](https://www.npmjs.com/package/minifyify)

[![apidoc](https://npmdoc.github.io/node-npmdoc-minifyify/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-minifyify_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-minifyify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-minifyify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-minifyify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ben Ng",
        "email": "me@benng.me",
        "url": "http://benng.me"
    },
    "bugs": {
        "url": "https://github.com/ben-ng/minifyify/issues"
    },
    "contributors": [
        {
            "name": "Jesús Leganés Combarro 'piranna'",
            "email": "piranna@gmail.com",
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
            "name": "benng",
            "email": "me@benng.me"
        }
    ],
    "name": "minifyify",
    "optionalDependencies": {},
    "peerDependencies": {
        "browserify": ">= 5"
    },
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module minifyify](#apidoc.module.minifyify)
1.  [function <span class="apidocSignatureSpan">minifyify.</span>minifier (opts)](#apidoc.element.minifyify.minifier)
1.  object <span class="apidocSignatureSpan">minifyify.</span>minifier.prototype

#### [module minifyify.minifier](#apidoc.module.minifyify.minifier)
1.  [function <span class="apidocSignatureSpan">minifyify.</span>minifier (opts)](#apidoc.element.minifyify.minifier.minifier)

#### [module minifyify.minifier.prototype](#apidoc.module.minifyify.minifier.prototype)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>codeForFile (file)](#apidoc.element.minifyify.minifier.prototype.codeForFile)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>consumer (cb)](#apidoc.element.minifyify.minifier.prototype.consumer)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>decoupleBundle (src)](#apidoc.element.minifyify.minifier.prototype.decoupleBundle)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>eachSource (cb)](#apidoc.element.minifyify.minifier.prototype.eachSource)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>fileExists (file)](#apidoc.element.minifyify.minifier.prototype.fileExists)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>mapForFile (file)](#apidoc.element.minifyify.minifier.prototype.mapForFile)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>normalizePath (file)](#apidoc.element.minifyify.minifier.prototype.normalizePath)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>registerMap (file, code, map)](#apidoc.element.minifyify.minifier.prototype.registerMap)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>sanitizeObject (opts)](#apidoc.element.minifyify.minifier.prototype.sanitizeObject)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>transformMap (bundleMap)](#apidoc.element.minifyify.minifier.prototype.transformMap)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>transformMapping (file, mapping, offset)](#apidoc.element.minifyify.minifier.prototype.transformMapping)
1.  [function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>transformer (file)](#apidoc.element.minifyify.minifier.prototype.transformer)



# <a name="apidoc.module.minifyify"></a>[module minifyify](#apidoc.module.minifyify)

#### <a name="apidoc.element.minifyify.minifier"></a>[function <span class="apidocSignatureSpan">minifyify.</span>minifier (opts)](#apidoc.element.minifyify.minifier)
- description and source-code
```javascript
minifier = function (opts) {
<span class="apidocCodeCommentSpan">  /*
  * Handle options/defaults
  */
</span>
  opts = opts || {};

  var defaults = {
        minify: true
      , source: 'bundle.js'
      , map: 'bundle.map'
      , sourcesContent: true
      , compressPath: function (filePath) {
          // noop
          return filePath;
        }
      }
  , compressTarget;

  this.opts = _.defaults(opts, defaults);

  /* Turn a string compressPath into a function */
  if(typeof this.opts.compressPath == 'string') {
    compressTarget = this.opts.compressPath;

    this.opts.compressPath = function (p) {
      return path.relative(compressTarget, p);
    }
  }

  /*
  * Instance variables
  */
  this.registry = {}; // Keep source maps and code by file

  /**
  * Browserify runs transforms with a different context
  * but we always want to refer to ourselves
  */
  this.transformer = _.bind(this.transformer, this);

  // Apply glob string include/exclude filters
  this.transformer = filter(this.transformer, {
    include : opts.include,
    exclude : opts.exclude,
    base    : opts.base
  });

  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.minifyify.minifier"></a>[module minifyify.minifier](#apidoc.module.minifyify.minifier)

#### <a name="apidoc.element.minifyify.minifier.minifier"></a>[function <span class="apidocSignatureSpan">minifyify.</span>minifier (opts)](#apidoc.element.minifyify.minifier.minifier)
- description and source-code
```javascript
minifier = function (opts) {
<span class="apidocCodeCommentSpan">  /*
  * Handle options/defaults
  */
</span>
  opts = opts || {};

  var defaults = {
        minify: true
      , source: 'bundle.js'
      , map: 'bundle.map'
      , sourcesContent: true
      , compressPath: function (filePath) {
          // noop
          return filePath;
        }
      }
  , compressTarget;

  this.opts = _.defaults(opts, defaults);

  /* Turn a string compressPath into a function */
  if(typeof this.opts.compressPath == 'string') {
    compressTarget = this.opts.compressPath;

    this.opts.compressPath = function (p) {
      return path.relative(compressTarget, p);
    }
  }

  /*
  * Instance variables
  */
  this.registry = {}; // Keep source maps and code by file

  /**
  * Browserify runs transforms with a different context
  * but we always want to refer to ourselves
  */
  this.transformer = _.bind(this.transformer, this);

  // Apply glob string include/exclude filters
  this.transformer = filter(this.transformer, {
    include : opts.include,
    exclude : opts.exclude,
    base    : opts.base
  });

  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.minifyify.minifier.prototype"></a>[module minifyify.minifier.prototype](#apidoc.module.minifyify.minifier.prototype)

#### <a name="apidoc.element.minifyify.minifier.prototype.codeForFile"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>codeForFile (file)](#apidoc.element.minifyify.minifier.prototype.codeForFile)
- description and source-code
```javascript
codeForFile = function (file) {
  if(!this.fileExists(file)) {
    throw new Error('ENOFILE');
  }

  return this.registry[file].code;
}
```
- example usage
```shell
...
/*
* Iterates over each code file, executes a function
*/
Minifier.prototype.eachSource = function (cb) {
  var self = this;

  _.each(Object.keys(this.registry).sort(), function(file) {
    cb(file, self.codeForFile(file), self.mapForFile(file));
  });
};

/*
* Given source with embedded sourcemap, seperate the two
* Returns the code and SourcemapConsumer object seperately
*/
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.consumer"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>consumer (cb)](#apidoc.element.minifyify.minifier.prototype.consumer)
- description and source-code
```javascript
consumer = function (cb) {
  var self = this;

  return concat(function(data) {
    if(!self.opts.minify) {
      // Keep browserify's sourcemap
      return cb(null, data.toString(), null);
    }
    else if (!self.opts.map) {
      // Remove browserify's inline sourcemap
      return cb(null, convertSM.removeComments(data.toString()), null);
    }
    else {
      var bundle = self.decoupleBundle(data);

      if(bundle === false) {
        if(self.opts.minify)
          throw new Error('Browserify must be in debug mode for minifyify to consume sourcemaps')

        return cb(null, convertSM.removeComments(data.toString()));
      }

      // Re-maps the browserify sourcemap
      // to the original source using the
      // uglify sourcemap
      bundle.map = self.transformMap(bundle.map);

      bundle.code = bundle.code + '\n//# sourceMappingURL=' + self.opts.map

      cb(null, bundle.code, bundle.map);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.minifyify.minifier.prototype.decoupleBundle"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>decoupleBundle (src)](#apidoc.element.minifyify.minifier.prototype.decoupleBundle)
- description and source-code
```javascript
decoupleBundle = function (src) {
  if(typeof src != 'string')
    src = src.toString();

  var map = convertSM.fromSource(src);
  // The source didn't have a sourcemap in it
  if(!map) {
    return false;
  }

  return {
    code: convertSM.removeComments(src)
  , map: new SMConsumer( map.toObject() )
  };
}
```
- example usage
```shell
...
return cb(null, data.toString(), null);
    }
    else if (!self.opts.map) {
// Remove browserify's inline sourcemap
return cb(null, convertSM.removeComments(data.toString()), null);
    }
    else {
var bundle = self.decoupleBundle(data);

if(bundle === false) {
  if(self.opts.minify)
    throw new Error('Browserify must be in debug mode for minifyify to consume sourcemaps')

  return cb(null, convertSM.removeComments(data.toString()));
}
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.eachSource"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>eachSource (cb)](#apidoc.element.minifyify.minifier.prototype.eachSource)
- description and source-code
```javascript
eachSource = function (cb) {
  var self = this;

  _.each(Object.keys(this.registry).sort(), function(file) {
    cb(file, self.codeForFile(file), self.mapForFile(file));
  });
}
```
- example usage
```shell
...
}

// Map from the hi-res sourcemaps to the browserify bundle
if(process.env.debug) {
  console.log(' [DEBUG] Here is how I\'m mapping your code:');
}

self.eachSource(function (file, code) {
  // Ignore files with no mappings
  if(!self.fileExists(file) || hasNoMappings(file)) {
    if(process.env.debug) {
      throw new Error('File with no mappings: ' + file)
    }
    return;
  }
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.fileExists"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>fileExists (file)](#apidoc.element.minifyify.minifier.prototype.fileExists)
- description and source-code
```javascript
fileExists = function (file) {
  return (this.registry[file] != null);
}
```
- example usage
```shell
...
  this.registry[file] = {code:code, map:map};
};

/*
* Gets map by file
*/
Minifier.prototype.mapForFile = function (file) {
  if(!this.fileExists(file)) {
    throw new Error('ENOFILE');
  }

  return this.registry[file].map;
};

/*
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.mapForFile"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>mapForFile (file)](#apidoc.element.minifyify.minifier.prototype.mapForFile)
- description and source-code
```javascript
mapForFile = function (file) {
  if(!this.fileExists(file)) {
    throw new Error('ENOFILE');
  }

  return this.registry[file].map;
}
```
- example usage
```shell
...
  if(process.env.debug) {
    throw new Error('File with no mappings: ' + file)
  }
  return;
}

var offset = lineForSource(file) - 1
  , fileMap = self.mapForFile(file)
  , transformedFileName = self.opts.compressPath(file);

if(process.env.debug) {
  console.log(' [DEBUG]  Now mapping "' + transformedFileName + '"');
}

fileMap.eachMapping(function (mapping) {
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.normalizePath"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>normalizePath (file)](#apidoc.element.minifyify.minifier.prototype.normalizePath)
- description and source-code
```javascript
normalizePath = function (file) {
  // Is file a relative path?
  if (!/^\w:|^\//.test(file)) {
    return file.replace(/\\/g, '/');
  }
  // Resolve absolute paths relative to basedir
  // Force '/' as path separator
  var basedir = this.opts.basedir || process.cwd();
  return path.relative(basedir, file).replace(/\\/g, '/');
}
```
- example usage
```shell
...
  , basedir = this.opts.basedir || process.cwd()
  , buffs = []
  , write
  , end
  , throughStream;

//Normalize the path separators to match what Browserify stores in the original Source Map
file = this.normalizePath(file);

write = function (data) {
  if(self.opts.minify) {
    buffs.push(data);
  }
  else {
    this.queue(data);
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.registerMap"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>registerMap (file, code, map)](#apidoc.element.minifyify.minifier.prototype.registerMap)
- description and source-code
```javascript
registerMap = function (file, code, map) {
  this.registry[file] = {code:code, map:map};
}
```
- example usage
```shell
...

try {
  var min = uglify.minify(unminCode, opts);

  thisStream.queue(convertSM.removeMapFileComments(min.code).trim());

  if(self.opts.map) {
    self.registerMap(file, originalCode || unminCode, new SMConsumer(min.map));
  }
}
catch(e) {
  console.error('uglify-js failed on '+file+' : ' + e.toString());
  thisStream.queue(unminCode);
}
finally {
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.sanitizeObject"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>sanitizeObject (opts)](#apidoc.element.minifyify.minifier.prototype.sanitizeObject)
- description and source-code
```javascript
sanitizeObject = function (opts) {
  if(opts._ !== undefined) delete opts._;
  for (var key in opts) {
    if(typeof opts[key] === 'object' && opts[key] != null) {
      this.sanitizeObject(opts[key]);
    }
  }
  return opts;
}
```
- example usage
```shell
...
        var opts = {
  fromString: true
, outSourceMap: (self.opts.map ? self.opts.map : undefined)
, inSourceMap: (self.opts.map ? tempExistingMapFile : undefined)
        };

        if (typeof self.opts.uglify === 'object') {
self.sanitizeObject(self.opts.uglify);
_.assign(opts, self.opts.uglify);
        }

        try {
var min = uglify.minify(unminCode, opts);

thisStream.queue(convertSM.removeMapFileComments(min.code).trim());
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.transformMap"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>transformMap (bundleMap)](#apidoc.element.minifyify.minifier.prototype.transformMap)
- description and source-code
```javascript
transformMap = function (bundleMap) {
  var self = this
    , generator = new SMGenerator({
        file: self.opts.source
      })
      // Map File -> The lowest numbered line in the bundle (offset)
    , bundleToMinMap = {}

<span class="apidocCodeCommentSpan">      /*
      * Helper function that maps minified source to a line in the browserify bundle
      */
</span>    , mapSourceToLine = function (source, line) {
        var target = bundleToMinMap[source];

        if(!target || target > line) {
          bundleToMinMap[source] = line;
        }
      }

    , hasNoMappings = function (file) {
        return bundleToMinMap[file] == null;
      }

      /*
      * Helper function that gets the line
      */
    , lineForSource = function (source) {
        if(hasNoMappings(source)) {
          throw new Error('ENOFILE: ' + source);
        }

        var target = bundleToMinMap[source];

        return target;
      }
    , missingSources = {};

  // Figure out where my minified files went in the bundle
  bundleMap.eachMapping(function (mapping) {
    var source = self.normalizePath(mapping.source);
    if(self.fileExists(source)) {
      mapSourceToLine(source, mapping.generatedLine);
    }
    // Not a known source, pass thru the mapping
    else {
      generator.addMapping({
        generated: {
          line: mapping.generatedLine
        , column: mapping.generatedColumn
        }
      , original: {
          line: mapping.originalLine
        , column: mapping.originalColumn
        }
      , source: self.opts.compressPath(mapping.source)
      , name: mapping.name
      });

      missingSources[mapping.source] = true;
    }
  });

  if(process.env.debug) {
    console.log(' [DEBUG] Here is where Browserify put your modules:');
    _.each(bundleToMinMap, function (line, file) {
      console.log(' [DEBUG] line ' + line + ' "' + self.opts.compressPath(file) + '"');
    });
  }

  // Add sourceContent for missing sources
  if (self.opts.sourcesContent) {
    _.each(missingSources, function (v, source) {
      generator.setSourceContent(self.opts.compressPath(source), bundleMap.sourceContentFor(source));
    });
  }

  // Map from the hi-res sourcemaps to the browserify bundle
  if(process.env.debug) {
    console.log(' [DEBUG] Here is how I\'m mapping your code:');
  }

  self.eachSource(function (file, code) {
    // Ignore files with no mappings
    if(!self.fileExists(file) || hasNoMappings(file)) {
      if(process.env.debug) {
        throw new Error('File with no mappings: ' + file)
      }
      return;
    }

    var offset = lineForSource(file) - 1
      , fileMap = self.mapForFile(file)
      , transformedFileName = self.opts.compressPath(file);

    if(process.env.debug) {
      console.log(' [DEBUG]  Now mapping "' + transformedFileName + '"');
    }

    fileMap.eachMapping(function (mapping) {
      var transformedMapping = self.transformMapping(transformedFileName, mapping, offset);

      if(process.env.debug) {
        console.log(' [DEBUG]  Generated [' + transformedMapping.generated.line +
           ':' + transformedMapping.generated.column + '] > [' +
           mapping.originalLine + ':' + mapping.originalColumn + '] Original');
      }

      generator.addMapping( transformedMapping );
    });

    if (self.opts.sourcesContent) {
      generator.setSourceContent(transformedFileName, code);
    }
  });

  return generator.toString();
}
```
- example usage
```shell
...

        return cb(null, convertSM.removeComments(data.toString()));
      }

      // Re-maps the browserify sourcemap
      // to the original source using the
      // uglify sourcemap
      bundle.map = self.transformMap(bundle.map);

      bundle.code = bundle.code + '\n//# sourceMappingURL=' + self.opts.map

      cb(null, bundle.code, bundle.map);
    }
  });
};
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.transformMapping"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>transformMapping (file, mapping, offset)](#apidoc.element.minifyify.minifier.prototype.transformMapping)
- description and source-code
```javascript
transformMapping = function (file, mapping, offset) {
  return {
    generated: {
      line: mapping.generatedLine + offset
    , column: mapping.generatedColumn
    }
  , original: {
      line: mapping.originalLine
    , column: mapping.originalColumn
    }
  , source: file
  , name: mapping.name
  }
}
```
- example usage
```shell
...
, transformedFileName = self.opts.compressPath(file);

    if(process.env.debug) {
console.log(' [DEBUG]  Now mapping "' + transformedFileName + '"');
    }

    fileMap.eachMapping(function (mapping) {
var transformedMapping = self.transformMapping(transformedFileName, mapping, offset);

if(process.env.debug) {
  console.log(' [DEBUG]  Generated [' + transformedMapping.generated.line +
     ':' + transformedMapping.generated.column + '] > [' +
     mapping.originalLine + ':' + mapping.originalColumn + '] Original');
}
...
```

#### <a name="apidoc.element.minifyify.minifier.prototype.transformer"></a>[function <span class="apidocSignatureSpan">minifyify.minifier.prototype.</span>transformer (file)](#apidoc.element.minifyify.minifier.prototype.transformer)
- description and source-code
```javascript
transformer = function (file) {
  var self = this
    , basedir = this.opts.basedir || process.cwd()
    , buffs = []
    , write
    , end
    , throughStream;

  //Normalize the path separators to match what Browserify stores in the original Source Map
  file = this.normalizePath(file);

  write = function (data) {
    if(self.opts.minify) {
      buffs.push(data);
    }
    else {
      this.queue(data);
    }
  }

  end = function () {
    if(self.opts.minify === false) {
      this.queue(null)
      return
    }

    var thisStream = this
      , unminCode = buffs.join('')
      , originalCode = false
      , existingMap = convertSM.fromSource(unminCode)
      , finish;

    existingMap = existingMap ? existingMap.toObject() : false;

    if(existingMap && existingMap.sourcesContent && existingMap.sourcesContent.length) {
      originalCode = convertSM.removeComments(existingMap.sourcesContent[0]);
      existingMap = JSON.stringify(existingMap);
    }
    // Only accept existing maps with sourcesContent
    else {
      existingMap = false;
    }

    finish = function (tempExistingMapFile, cleanupCallback) {
      // Don't minify JSON!
      if(file.match(/\.json$/)) {
        try {
          thisStream.queue(JSON.stringify(JSON.parse(unminCode)))
        }
        catch(e) {
          console.error('failed to parse JSON in ' + file)
          thisStream.queue(unminCode)
        }
      }
      else if (file.match(/\.css$/)) {
        thisStream.queue(unminCode)
      }
      else {
        var opts = {
            fromString: true
          , outSourceMap: (self.opts.map ? self.opts.map : undefined)
          , inSourceMap: (self.opts.map ? tempExistingMapFile : undefined)
        };

        if (typeof self.opts.uglify === 'object') {
          self.sanitizeObject(self.opts.uglify);
          _.assign(opts, self.opts.uglify);
        }

        try {
          var min = uglify.minify(unminCode, opts);

          thisStream.queue(convertSM.removeMapFileComments(min.code).trim());

          if(self.opts.map) {
            self.registerMap(file, originalCode || unminCode, new SMConsumer(min.map));
          }
        }
        catch(e) {
          console.error('uglify-js failed on '+file+' : ' + e.toString());
          thisStream.queue(unminCode);
        }
        finally {
          if (typeof cleanupCallback === 'function') {
            cleanupCallback();
          }
        }
      }

      // Otherwise we'll never finish
      thisStream.queue(null);
    }

    if(existingMap) {
      tmp.file(function (err, path, fd, cleanupCallback) {
        if(err) {
          cleanupCallback();
          throw err;
        }

        fs.writeFile(path, existingMap, function (err) {
          if(err) {
            cleanupCallback();
            throw err;
          }
          finish(path, cleanupCallback);
        });
      });
    }
    else {
      finish();
    }
  }

  throughStream = through(write, end);

  throughStream.call = function () {
    throw new Error('Transformer is a transform. Correct usage: 'bundle.transform(minifier.transformer)'.')
  }

  return throughStream;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
