# vrjs/axis
Simple utility to build a THREE.js 3D axis object.  The module uses node's require
module pattern - it should be run within something like [nw](http://nwjs.io/)

## Usage
The export is a constructor which accepts a reference to THREE.  The constructor
returns a single object that has a `make` functions which returns the axis.

```js

var axis = require('..')(THREE);
mesh.add(axis.make());

```
See [example](example/) for more context.

## Options
The `make` function can accept an options object.  The following properties are supported:

- **neg**:  boolean value, indicating if negative dimensions (dashed) should be shown.  Default is false
- **length**:  length (pixels) of axes.  Default is 250

```
var axis = require('..')(THREE);
mesh.add(axis.make({neg:true, length:300}));
```