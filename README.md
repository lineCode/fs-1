
# then-fs

  Promised version of the node.js `fs` module.
  All non-callback-taking functions of fs are simply inherited.

[![Build Status](https://img.shields.io/travis/then/fs/master.svg)](https://travis-ci.org/then/fs)
[![Dependency Status](https://img.shields.io/david/then/fs.svg)](https://david-dm.org/then/fs)
[![NPM version](https://badge.fury.io/js/then-fs.png)](http://badge.fury.io/js/then-fs)

## Installation

    $ npm install then-fs

## API

  The API for `then-fs` is exactly that of the built in `fs` module except that any function which normally takes a callback returns a promise instead.

  Example:

```js
function readJSON(path) {
  return fs.readFile(path, 'utf8').then(JSON.parse)
}
readJSON(__dirname + '/package.json')
  .done(function (obj) {
    console.dir(oj)
  })
```

## License

  MIT
