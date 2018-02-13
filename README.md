# xmlrpc-lite

[![npm](https://img.shields.io/npm/v/xmlrpc-lite.svg)](https://www.npmjs.com/package/xmlrpc-lite)
[![Build Status](https://travis-ci.org/wangzuo/xmlrpc-lite.svg?branch=master)](https://travis-ci.org/wangzuo/xmlrpc-lite)
[![codecov](https://codecov.io/gh/wangzuo/xmlrpc-lite/branch/master/graph/badge.svg)](https://codecov.io/gh/wangzuo/xmlrpc-lite)
[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

Simple xmlrpc client for node and browser

* Object params support via `<struct>`
* String type support only

### Installation

```sh
npm install xmlrpc-lite --save
```

### Example

```javascript
// xmlrpc request to ipboard forum
var Client = require('xmlrpc-lite');
var t = new Client('http://forum/interface/board/index.php');
t.call(
  'loginUser',
  {
    id: 'xxxx',
    api_module: 'ipb',
    api_key: 'xxxxxx'
  },
  function(err, xml) {
    if (err) throw err;
    console.log(xml);
  }
);
```

### License

ISC
