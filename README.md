# Pkgm

[![Build Status](https://travis-ci.org/CodeboxIDE/pkgm.png?branch=master)](https://travis-ci.org/CodeboxIDE/pkgm) [![Greenkeeper badge](https://badges.greenkeeper.io/uniibu/ds-pkgm.svg)](https://greenkeeper.io/)

Make it easy to build a package manager for client/node large applications.

## How to use it?

#### Installation

```
$ npm install pkgm
```

#### Load packages

```js
var Pkgm = require("pkgm");
var pkg = require("./package.json");

var manager = new Pkgm({
    'engine': "my-engine",
    'version': pkg.version,
    'folder': path.resolve(__dirname, "./packages")
});

manager.prepare(pkg.packageDependencies)
.then(function() {
    console.log("package ready and built!");
});
```

