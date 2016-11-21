## HTTP 路径代理

解决 跨域问题


### from 

[Array<string>]

需要代理的路径，支持正则表达式字符串

### to

实际导向的路径.


### attribute

正则表达式的属性值，可选。

### options

可选。 见 https://github.com/nodejitsu/node-http-proxy#options


## e.g.

大小写不敏感的路径匹配，  将 以`/p/`, `/api/`开始的路径 代理到  `http://example.com`

```js
 "proxy": [{
    "from": ["^/p", "^/api"], // or "^/p"
    "attribute": "i", // optional
    "to": "http://example.com" 
    // or replace 'to' attr
    //"options": {xxx}  // https://github.com/nodejitsu/node-http-proxy#options
  }]
```