# api documentation for  [request (v2.81.0)](https://github.com/request/request#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-request.svg)](https://travis-ci.org/npmdoc/node-npmdoc-request)
#### Simplified HTTP request client.

[![NPM](https://nodei.co/npm/request.png?downloads=true)](https://www.npmjs.com/package/request)

[![apidoc](https://npmdoc.github.io/node-npmdoc-request/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-request_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-request/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-request/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Mikeal Rogers",
        "email": "mikeal.rogers@gmail.com"
    },
    "bugs": {
        "url": "http://github.com/request/request/issues"
    },
    "dependencies": {
        "aws-sign2": "~0.6.0",
        "aws4": "^1.2.1",
        "caseless": "~0.12.0",
        "combined-stream": "~1.0.5",
        "extend": "~3.0.0",
        "forever-agent": "~0.6.1",
        "form-data": "~2.1.1",
        "har-validator": "~4.2.1",
        "hawk": "~3.1.3",
        "http-signature": "~1.1.0",
        "is-typedarray": "~1.0.0",
        "isstream": "~0.1.2",
        "json-stringify-safe": "~5.0.1",
        "mime-types": "~2.1.7",
        "oauth-sign": "~0.8.1",
        "performance-now": "^0.2.0",
        "qs": "~6.4.0",
        "safe-buffer": "^5.0.1",
        "stringstream": "~0.0.4",
        "tough-cookie": "~2.3.0",
        "tunnel-agent": "^0.6.0",
        "uuid": "^3.0.0"
    },
    "description": "Simplified HTTP request client.",
    "devDependencies": {
        "bluebird": "^3.2.1",
        "browserify": "^13.0.1",
        "browserify-istanbul": "^2.0.0",
        "buffer-equal": "^1.0.0",
        "codecov": "^1.0.1",
        "coveralls": "^2.11.4",
        "eslint": "^2.5.3",
        "function-bind": "^1.0.2",
        "istanbul": "^0.4.0",
        "karma": "^1.1.1",
        "karma-browserify": "^5.0.1",
        "karma-cli": "^1.0.0",
        "karma-coverage": "^1.0.0",
        "karma-phantomjs-launcher": "^1.0.0",
        "karma-tap": "^3.0.1",
        "phantomjs-prebuilt": "^2.1.3",
        "rimraf": "^2.2.8",
        "server-destroy": "^1.0.1",
        "tape": "^4.6.0",
        "taper": "^0.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "c6928946a0e06c5f8d6f8a9333469ffda46298a0",
        "tarball": "https://registry.npmjs.org/request/-/request-2.81.0.tgz"
    },
    "engines": {
        "node": ">= 4"
    },
    "files": [
        "lib/",
        "index.js",
        "request.js"
    ],
    "gitHead": "a0cdc704c19e63e6f1740e173bb003c51eef524c",
    "greenkeeper": {
        "ignore": [
            "eslint",
            "hawk",
            "har-validator"
        ]
    },
    "homepage": "https://github.com/request/request#readme",
    "keywords": [
        "http",
        "simple",
        "util",
        "utility"
    ],
    "license": "Apache-2.0",
    "main": "index.js",
    "maintainers": [
        {
            "name": "mikeal",
            "email": "mikeal.rogers@gmail.com"
        },
        {
            "name": "nylen",
            "email": "jnylen@gmail.com"
        },
        {
            "name": "fredkschott",
            "email": "fkschott@gmail.com"
        },
        {
            "name": "simov",
            "email": "simeonvelichkov@gmail.com"
        }
    ],
    "name": "request",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/request/request.git"
    },
    "scripts": {
        "lint": "eslint lib/ *.js tests/ && echo Lint passed.",
        "test": "npm run lint && npm run test-ci && npm run test-browser",
        "test-browser": "node tests/browser/start.js",
        "test-ci": "taper tests/test-*.js",
        "test-cov": "istanbul cover tape tests/test-*.js"
    },
    "version": "2.81.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module request](#apidoc.module.request)
1.  [function <span class="apidocSignatureSpan">request.</span>Request (options)](#apidoc.element.request.Request)
1.  [function <span class="apidocSignatureSpan">request.</span>cookie (str)](#apidoc.element.request.cookie)
1.  [function <span class="apidocSignatureSpan">request.</span>defaults (options, requester)](#apidoc.element.request.defaults)
1.  [function <span class="apidocSignatureSpan">request.</span>del (uri, options, callback)](#apidoc.element.request.del)
1.  [function <span class="apidocSignatureSpan">request.</span>delete (uri, options, callback)](#apidoc.element.request.delete)
1.  [function <span class="apidocSignatureSpan">request.</span>forever (agentOptions, optionsArg)](#apidoc.element.request.forever)
1.  [function <span class="apidocSignatureSpan">request.</span>get (uri, options, callback)](#apidoc.element.request.get)
1.  [function <span class="apidocSignatureSpan">request.</span>head (uri, options, callback)](#apidoc.element.request.head)
1.  [function <span class="apidocSignatureSpan">request.</span>initParams (uri, options, callback)](#apidoc.element.request.initParams)
1.  [function <span class="apidocSignatureSpan">request.</span>jar (store)](#apidoc.element.request.jar)
1.  [function <span class="apidocSignatureSpan">request.</span>patch (uri, options, callback)](#apidoc.element.request.patch)
1.  [function <span class="apidocSignatureSpan">request.</span>post (uri, options, callback)](#apidoc.element.request.post)
1.  [function <span class="apidocSignatureSpan">request.</span>put (uri, options, callback)](#apidoc.element.request.put)
1.  object <span class="apidocSignatureSpan">request.</span>Request.prototype
1.  object <span class="apidocSignatureSpan">request.</span>auth
1.  object <span class="apidocSignatureSpan">request.</span>cookies
1.  object <span class="apidocSignatureSpan">request.</span>har
1.  object <span class="apidocSignatureSpan">request.</span>helpers
1.  object <span class="apidocSignatureSpan">request.</span>multipart
1.  object <span class="apidocSignatureSpan">request.</span>oauth
1.  object <span class="apidocSignatureSpan">request.</span>querystring
1.  object <span class="apidocSignatureSpan">request.</span>redirect
1.  object <span class="apidocSignatureSpan">request.</span>tunnel

#### [module request.Request](#apidoc.module.request.Request)
1.  [function <span class="apidocSignatureSpan">request.</span>Request (options)](#apidoc.element.request.Request.Request)
1.  [function <span class="apidocSignatureSpan">request.Request.</span>super_ ()](#apidoc.element.request.Request.super_)
1.  object <span class="apidocSignatureSpan">request.Request.</span>defaultProxyHeaderExclusiveList
1.  object <span class="apidocSignatureSpan">request.Request.</span>defaultProxyHeaderWhiteList

#### [module request.Request.prototype](#apidoc.module.request.Request.prototype)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>abort ()](#apidoc.element.request.Request.prototype.abort)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>auth (user, pass, sendImmediately, bearer)](#apidoc.element.request.Request.prototype.auth)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>aws (opts, now)](#apidoc.element.request.Request.prototype.aws)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>debug ()](#apidoc.element.request.Request.prototype.debug)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>destroy ()](#apidoc.element.request.Request.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>enableUnixSocket ()](#apidoc.element.request.Request.prototype.enableUnixSocket)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>end (chunk)](#apidoc.element.request.Request.prototype.end)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>form (form)](#apidoc.element.request.Request.prototype.form)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>getHeader (name, headers)](#apidoc.element.request.Request.prototype.getHeader)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>getNewAgent ()](#apidoc.element.request.Request.prototype.getNewAgent)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>hawk (opts)](#apidoc.element.request.Request.prototype.hawk)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>httpSignature (opts)](#apidoc.element.request.Request.prototype.httpSignature)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>init (options)](#apidoc.element.request.Request.prototype.init)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>jar (jar)](#apidoc.element.request.Request.prototype.jar)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>json (val)](#apidoc.element.request.Request.prototype.json)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>multipart (multipart)](#apidoc.element.request.Request.prototype.multipart)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>oauth (_oauth)](#apidoc.element.request.Request.prototype.oauth)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>onRequestError (error)](#apidoc.element.request.Request.prototype.onRequestError)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>onRequestResponse (response)](#apidoc.element.request.Request.prototype.onRequestResponse)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>pause ()](#apidoc.element.request.Request.prototype.pause)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>pipe (dest, opts)](#apidoc.element.request.Request.prototype.pipe)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>pipeDest (dest)](#apidoc.element.request.Request.prototype.pipeDest)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>qs (q, clobber)](#apidoc.element.request.Request.prototype.qs)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>readResponseBody (response)](#apidoc.element.request.Request.prototype.readResponseBody)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>resume ()](#apidoc.element.request.Request.prototype.resume)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>start ()](#apidoc.element.request.Request.prototype.start)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>toJSON ()](#apidoc.element.request.Request.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">request.Request.prototype.</span>write ()](#apidoc.element.request.Request.prototype.write)

#### [module request.auth](#apidoc.module.request.auth)
1.  [function <span class="apidocSignatureSpan">request.auth.</span>Auth (request)](#apidoc.element.request.auth.Auth)

#### [module request.cookies](#apidoc.module.request.cookies)
1.  [function <span class="apidocSignatureSpan">request.cookies.</span>jar (store)](#apidoc.element.request.cookies.jar)
1.  [function <span class="apidocSignatureSpan">request.cookies.</span>parse (str)](#apidoc.element.request.cookies.parse)

#### [module request.har](#apidoc.module.request.har)
1.  [function <span class="apidocSignatureSpan">request.har.</span>Har (request)](#apidoc.element.request.har.Har)

#### [module request.helpers](#apidoc.module.request.helpers)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>copy (obj)](#apidoc.element.request.helpers.copy)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>defer (callback, arg1, arg2, arg3)](#apidoc.element.request.helpers.defer)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>isReadStream (rs)](#apidoc.element.request.helpers.isReadStream)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>md5 (str)](#apidoc.element.request.helpers.md5)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>paramsHaveRequestBody (params)](#apidoc.element.request.helpers.paramsHaveRequestBody)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>safeStringify (obj, replacer)](#apidoc.element.request.helpers.safeStringify)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>toBase64 (str)](#apidoc.element.request.helpers.toBase64)
1.  [function <span class="apidocSignatureSpan">request.helpers.</span>version ()](#apidoc.element.request.helpers.version)

#### [module request.multipart](#apidoc.module.request.multipart)
1.  [function <span class="apidocSignatureSpan">request.multipart.</span>Multipart (request)](#apidoc.element.request.multipart.Multipart)

#### [module request.oauth](#apidoc.module.request.oauth)
1.  [function <span class="apidocSignatureSpan">request.oauth.</span>OAuth (request)](#apidoc.element.request.oauth.OAuth)

#### [module request.querystring](#apidoc.module.request.querystring)
1.  [function <span class="apidocSignatureSpan">request.querystring.</span>Querystring (request)](#apidoc.element.request.querystring.Querystring)

#### [module request.redirect](#apidoc.module.request.redirect)
1.  [function <span class="apidocSignatureSpan">request.redirect.</span>Redirect (request)](#apidoc.element.request.redirect.Redirect)

#### [module request.tunnel](#apidoc.module.request.tunnel)
1.  [function <span class="apidocSignatureSpan">request.tunnel.</span>Tunnel (request)](#apidoc.element.request.tunnel.Tunnel)



# <a name="apidoc.module.request"></a>[module request](#apidoc.module.request)

#### <a name="apidoc.element.request.Request"></a>[function <span class="apidocSignatureSpan">request.</span>Request (options)](#apidoc.element.request.Request)
- description and source-code
```javascript
function Request(options) {
  // if given the method property in options, set property explicitMethod to true

  // extend the Request instance with any non-reserved properties
  // remove any reserved functions from the options object
  // set Request instance to be readable and writable
  // call init

  var self = this

  // start with HAR, then override with additional options
  if (options.har) {
    self._har = new Har(self)
    options = self._har.options(options)
  }

  stream.Stream.call(self)
  var reserved = Object.keys(Request.prototype)
  var nonReserved = filterForNonReserved(reserved, options)

  extend(self, nonReserved)
  options = filterOutReservedFunctions(reserved, options)

  self.readable = true
  self.writable = true
  if (options.method) {
    self.explicitMethod = true
  }
  self._qs = new Querystring(self)
  self._auth = new Auth(self)
  self._oauth = new OAuth(self)
  self._multipart = new Multipart(self)
  self._redirect = new Redirect(self)
  self._tunnel = new Tunnel(self)
  self.init(options)
}
```
- example usage
```shell
...

var params = initParams(uri, options, callback)

if (params.method === 'HEAD' && paramsHaveRequestBody(params)) {
  throw new Error('HTTP HEAD requests MUST NOT include a request body.')
}

return new request.Request(params)
}

function verbFunc (verb) {
var method = verb.toUpperCase()
return function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
...
```

#### <a name="apidoc.element.request.cookie"></a>[function <span class="apidocSignatureSpan">request.</span>cookie (str)](#apidoc.element.request.cookie)
- description and source-code
```javascript
cookie = function (str) {
  return cookies.parse(str)
}
```
- example usage
```shell
...
request.get(url)
'''
### request.cookie

Function that creates a new cookie.

'''js
request.cookie('key1=value1')
'''
### request.jar()

Function that creates a new cookie jar.

'''js
request.jar()
...
```

#### <a name="apidoc.element.request.defaults"></a>[function <span class="apidocSignatureSpan">request.</span>defaults (options, requester)](#apidoc.element.request.defaults)
- description and source-code
```javascript
defaults = function (options, requester) {
  var self = this

  options = options || {}

  if (typeof options === 'function') {
    requester = options
    options = {}
  }

  var defaults      = wrapRequestMethod(self, options, requester)

  var verbs = ['get', 'head', 'post', 'put', 'patch', 'del', 'delete']
  verbs.forEach(function(verb) {
    defaults[verb]  = wrapRequestMethod(self[verb], options, requester, verb)
  })

  defaults.cookie   = wrapRequestMethod(self.cookie, options, requester)
  defaults.jar      = self.jar
  defaults.defaults = self.defaults
  return defaults
}
```
- example usage
```shell
...
'''js
req.pipe(request('http://mysite.com/doodle.png')).pipe(resp)
'''

Also, none of this new functionality conflicts with requests previous features, it just expands them.

'''js
var r = request.defaults({'proxy':'http://localproxy.com'})

http.createServer(function (req, resp) {
  if (req.url === '/doodle.png') {
    r.get('http://google.com/doodle.png').pipe(resp)
  }
})
'''
...
```

#### <a name="apidoc.element.request.del"></a>[function <span class="apidocSignatureSpan">request.</span>del (uri, options, callback)](#apidoc.element.request.del)
- description and source-code
```javascript
del = function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
  return request(params, params.callback)
}
```
- example usage
```shell
...
'''

### request.del / request.delete

Same as 'request()', but defaults to 'method: "DELETE"'.

'''js
request.del(url)
request.delete(url)
'''

### request.get

Same as 'request()' (for uniformity).
...
```

#### <a name="apidoc.element.request.delete"></a>[function <span class="apidocSignatureSpan">request.</span>delete (uri, options, callback)](#apidoc.element.request.delete)
- description and source-code
```javascript
delete = function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
  return request(params, params.callback)
}
```
- example usage
```shell
...

### request.del / request.delete

Same as 'request()', but defaults to 'method: "DELETE"'.

'''js
request.del(url)
request.delete(url)
'''

### request.get

Same as 'request()' (for uniformity).

'''js
...
```

#### <a name="apidoc.element.request.forever"></a>[function <span class="apidocSignatureSpan">request.</span>forever (agentOptions, optionsArg)](#apidoc.element.request.forever)
- description and source-code
```javascript
forever = function (agentOptions, optionsArg) {
  var options = {}
  if (optionsArg) {
    extend(options, optionsArg)
  }
  if (agentOptions) {
    options.agentOptions = agentOptions
  }

  options.forever = true
  return request.defaults(options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.get"></a>[function <span class="apidocSignatureSpan">request.</span>get (uri, options, callback)](#apidoc.element.request.get)
- description and source-code
```javascript
get = function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
  return request(params, params.callback)
}
```
- example usage
```shell
...
'''js
fs.createReadStream('file.json').pipe(request.put('http://mysite.com/obj.json'))
'''

Request can also 'pipe' to itself. When doing so, 'content-type' and 'content-length' are preserved in the PUT headers.

'''js
request.get('http://google.com/img.png').pipe(request.put('http://mysite.com/img.png'))
'''

Request emits a "response" event when a response is received. The 'response' argument will be an instance of [http.IncomingMessage
](https://nodejs.org/api/http.html#http_class_http_incomingmessage).

'''js
request
.get('http://google.com/img.png')
...
```

#### <a name="apidoc.element.request.head"></a>[function <span class="apidocSignatureSpan">request.</span>head (uri, options, callback)](#apidoc.element.request.head)
- description and source-code
```javascript
head = function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
  return request(params, params.callback)
}
```
- example usage
```shell
...
'''

### request.head

Same as 'request()', but defaults to 'method: "HEAD"'.

'''js
request.head(url)
'''

### request.del / request.delete

Same as 'request()', but defaults to 'method: "DELETE"'.

'''js
...
```

#### <a name="apidoc.element.request.initParams"></a>[function <span class="apidocSignatureSpan">request.</span>initParams (uri, options, callback)](#apidoc.element.request.initParams)
- description and source-code
```javascript
function initParams(uri, options, callback) {
  if (typeof options === 'function') {
    callback = options
  }

  var params = {}
  if (typeof options === 'object') {
    extend(params, options, {uri: uri})
  } else if (typeof uri === 'string') {
    extend(params, {uri: uri})
  } else {
    extend(params, uri)
  }

  params.callback = callback || params.callback
  return params
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.jar"></a>[function <span class="apidocSignatureSpan">request.</span>jar (store)](#apidoc.element.request.jar)
- description and source-code
```javascript
jar = function (store) {
  return cookies.jar(store)
}
```
- example usage
```shell
...
### request.cookie

Function that creates a new cookie.

'''js
request.cookie('key1=value1')
'''
### request.jar()

Function that creates a new cookie jar.

'''js
request.jar()
'''
...
```

#### <a name="apidoc.element.request.patch"></a>[function <span class="apidocSignatureSpan">request.</span>patch (uri, options, callback)](#apidoc.element.request.patch)
- description and source-code
```javascript
patch = function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
  return request(params, params.callback)
}
```
- example usage
```shell
...
'''

### request.patch

Same as 'request()', but defaults to 'method: "PATCH"'.

'''js
request.patch(url)
'''

### request.post

Same as 'request()', but defaults to 'method: "POST"'.

'''js
...
```

#### <a name="apidoc.element.request.post"></a>[function <span class="apidocSignatureSpan">request.</span>post (uri, options, callback)](#apidoc.element.request.post)
- description and source-code
```javascript
post = function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
  return request(params, params.callback)
}
```
- example usage
```shell
...


#### application/x-www-form-urlencoded (URL-Encoded Forms)

URL-encoded forms are simple.

'''js
request.post('http://service.com/upload', {form:{key:'value'}})
// or
request.post('http://service.com/upload').form({key:'value'})
// or
request.post({url:'http://service.com/upload', form: {key:'value'}}, function(err,httpResponse,body){ /* ... */ })
'''
...
```

#### <a name="apidoc.element.request.put"></a>[function <span class="apidocSignatureSpan">request.</span>put (uri, options, callback)](#apidoc.element.request.put)
- description and source-code
```javascript
put = function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
  return request(params, params.callback)
}
```
- example usage
```shell
...
'''js
request('http://google.com/doodle.png').pipe(fs.createWriteStream('doodle.png'))
'''

You can also stream a file to a PUT or POST request. This method will also check the file extension against a mapping of file extensions
 to content-types (in this case 'application/json') and use the proper 'content-type' in the PUT request (if the headers don’t already
 provide one).

'''js
fs.createReadStream('file.json').pipe(request.put('http://mysite.com/obj.json'))
'''

Request can also 'pipe' to itself. When doing so, 'content-type' and 'content-length' are preserved in the PUT headers.

'''js
request.get('http://google.com/img.png').pipe(request.put('http://mysite.com/img.png'))
'''
...
```



# <a name="apidoc.module.request.Request"></a>[module request.Request](#apidoc.module.request.Request)

#### <a name="apidoc.element.request.Request.Request"></a>[function <span class="apidocSignatureSpan">request.</span>Request (options)](#apidoc.element.request.Request.Request)
- description and source-code
```javascript
function Request(options) {
  // if given the method property in options, set property explicitMethod to true

  // extend the Request instance with any non-reserved properties
  // remove any reserved functions from the options object
  // set Request instance to be readable and writable
  // call init

  var self = this

  // start with HAR, then override with additional options
  if (options.har) {
    self._har = new Har(self)
    options = self._har.options(options)
  }

  stream.Stream.call(self)
  var reserved = Object.keys(Request.prototype)
  var nonReserved = filterForNonReserved(reserved, options)

  extend(self, nonReserved)
  options = filterOutReservedFunctions(reserved, options)

  self.readable = true
  self.writable = true
  if (options.method) {
    self.explicitMethod = true
  }
  self._qs = new Querystring(self)
  self._auth = new Auth(self)
  self._oauth = new OAuth(self)
  self._multipart = new Multipart(self)
  self._redirect = new Redirect(self)
  self._tunnel = new Tunnel(self)
  self.init(options)
}
```
- example usage
```shell
...

var params = initParams(uri, options, callback)

if (params.method === 'HEAD' && paramsHaveRequestBody(params)) {
  throw new Error('HTTP HEAD requests MUST NOT include a request body.')
}

return new request.Request(params)
}

function verbFunc (verb) {
var method = verb.toUpperCase()
return function (uri, options, callback) {
  var params = initParams(uri, options, callback)
  params.method = method
...
```

#### <a name="apidoc.element.request.Request.super_"></a>[function <span class="apidocSignatureSpan">request.Request.</span>super_ ()](#apidoc.element.request.Request.super_)
- description and source-code
```javascript
function Stream() {
  EE.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.Request.prototype"></a>[module request.Request.prototype](#apidoc.module.request.Request.prototype)

#### <a name="apidoc.element.request.Request.prototype.abort"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>abort ()](#apidoc.element.request.Request.prototype.abort)
- description and source-code
```javascript
abort = function () {
  var self = this
  self._aborted = true

  if (self.req) {
    self.req.abort()
  }
  else if (self.response) {
    self.response.destroy()
  }

  self.emit('abort')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.auth"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>auth (user, pass, sendImmediately, bearer)](#apidoc.element.request.Request.prototype.auth)
- description and source-code
```javascript
auth = function (user, pass, sendImmediately, bearer) {
  var self = this

  self._auth.onRequest(user, pass, sendImmediately, bearer)

  return self
}
```
- example usage
```shell
...

---


## HTTP Authentication

'''js
request.get('http://some.server.com/').auth('username', 'password', false);
// or
request.get('http://some.server.com/', {
'auth': {
  'user': 'username',
  'pass': 'password',
  'sendImmediately': false
}
...
```

#### <a name="apidoc.element.request.Request.prototype.aws"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>aws (opts, now)](#apidoc.element.request.Request.prototype.aws)
- description and source-code
```javascript
aws = function (opts, now) {
  var self = this

  if (!now) {
    self._aws = opts
    return self
  }

  if (opts.sign_version == 4 || opts.sign_version == '4') {
    // use aws4
    var options = {
      host: self.uri.host,
      path: self.uri.path,
      method: self.method,
      headers: {
        'content-type': self.getHeader('content-type') || ''
      },
      body: self.body
    }
    var signRes = aws4.sign(options, {
      accessKeyId: opts.key,
      secretAccessKey: opts.secret,
      sessionToken: opts.session
    })
    self.setHeader('authorization', signRes.headers.Authorization)
    self.setHeader('x-amz-date', signRes.headers['X-Amz-Date'])
    if (signRes.headers['X-Amz-Security-Token']) {
      self.setHeader('x-amz-security-token', signRes.headers['X-Amz-Security-Token'])
    }
  }
  else {
    // default: use aws-sign2
    var date = new Date()
    self.setHeader('date', date.toUTCString())
    var auth =
      { key: opts.key
      , secret: opts.secret
      , verb: self.method.toUpperCase()
      , date: date
      , contentType: self.getHeader('content-type') || ''
      , md5: self.getHeader('content-md5') || ''
      , amazonHeaders: aws2.canonicalizeHeaders(self.headers)
      }
    var path = self.uri.path
    if (opts.bucket && path) {
      auth.resource = '/' + opts.bucket + path
    } else if (opts.bucket && !path) {
      auth.resource = '/' + opts.bucket
    } else if (!opts.bucket && path) {
      auth.resource = path
    } else if (!opts.bucket && !path) {
      auth.resource = '/'
    }
    auth.resource = aws2.canonicalizeResource(auth.resource)
    self.setHeader('authorization', aws2.authorization(auth))
  }

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.debug"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>debug ()](#apidoc.element.request.Request.prototype.debug)
- description and source-code
```javascript
function debug() {
  if (Request.debug) {
    console.error('REQUEST %s', util.format.apply(util, arguments))
  }
}
```
- example usage
```shell
...

  if (!self.hasAuth || self.sentAuth) { return null }

  var c = caseless(response.headers)

  var authHeader = c.get('www-authenticate')
  var authVerb = authHeader && authHeader.split(' ')[0].toLowerCase()
  request.debug('reauth', authVerb)

  switch (authVerb) {
case 'basic':
  return self.basic(self.user, self.pass, true)

case 'bearer':
  return self.bearer(self.bearerToken, true)
...
```

#### <a name="apidoc.element.request.Request.prototype.destroy"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>destroy ()](#apidoc.element.request.Request.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  var self = this
  if (!self._ended) {
    self.end()
  } else if (self.response) {
    self.response.destroy()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.enableUnixSocket"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>enableUnixSocket ()](#apidoc.element.request.Request.prototype.enableUnixSocket)
- description and source-code
```javascript
enableUnixSocket = function () {
  // Get the socket & request paths from the URL
  var unixParts = this.uri.path.split(':')
    , host = unixParts[0]
    , path = unixParts[1]
  // Apply unix properties to request
  this.socketPath = host
  this.uri.pathname = path
  this.uri.path = path
  this.uri.host = host
  this.uri.hostname = host
  this.uri.isUnix = true
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.end"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>end (chunk)](#apidoc.element.request.Request.prototype.end)
- description and source-code
```javascript
end = function (chunk) {
  var self = this
  if (self._aborted) {return}

  if (chunk) {
    self.write(chunk)
  }
  if (!self._started) {
    self.start()
  }
  if (self.req) {
    self.req.end()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.form"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>form (form)](#apidoc.element.request.Request.prototype.form)
- description and source-code
```javascript
form = function (form) {
  var self = this
  if (form) {
    if (!/^application\/x-www-form-urlencoded\b/.test(self.getHeader('content-type'))) {
      self.setHeader('content-type', 'application/x-www-form-urlencoded')
    }
    self.body = (typeof form === 'string')
      ? self._qs.rfc3986(form.toString('utf8'))
      : self._qs.stringify(form).toString('utf8')
    return self
  }
  // create form-data object
  self._form = new FormData()
  self._form.on('error', function(err) {
    err.message = 'form-data: ' + err.message
    self.emit('error', err)
    self.abort()
  })
  return self._form
}
```
- example usage
```shell
...
#### application/x-www-form-urlencoded (URL-Encoded Forms)

URL-encoded forms are simple.

'''js
request.post('http://service.com/upload', {form:{key:'value'}})
// or
request.post('http://service.com/upload').form({key:'value'})
// or
request.post({url:'http://service.com/upload', form: {key:'value'}}, function(err,httpResponse,body){ /* ... */ })
'''


#### multipart/form-data (Multipart Form Uploads)
...
```

#### <a name="apidoc.element.request.Request.prototype.getHeader"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>getHeader (name, headers)](#apidoc.element.request.Request.prototype.getHeader)
- description and source-code
```javascript
getHeader = function (name, headers) {
  var self = this
  var result, re, match
  if (!headers) {
    headers = self.headers
  }
  Object.keys(headers).forEach(function (key) {
    if (key.length !== name.length) {
      return
    }
    re = new RegExp(name, 'i')
    match = key.match(re)
    if (match) {
      result = headers[key]
    }
  })
  return result
}
```
- example usage
```shell
...
  self.request.emit('error', new Error('Argument error, options.multipart.'))
}

if (options.chunked !== undefined) {
  chunked = options.chunked
}

if (self.request.getHeader('transfer-encoding') === 'chunked') {
  chunked = true
}

if (!chunked) {
  parts.forEach(function (part) {
    if (typeof part.body === 'undefined') {
      self.request.emit('error', new Error('Body attribute missing in multipart.'))
...
```

#### <a name="apidoc.element.request.Request.prototype.getNewAgent"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>getNewAgent ()](#apidoc.element.request.Request.prototype.getNewAgent)
- description and source-code
```javascript
getNewAgent = function () {
  var self = this
  var Agent = self.agentClass
  var options = {}
  if (self.agentOptions) {
    for (var i in self.agentOptions) {
      options[i] = self.agentOptions[i]
    }
  }
  if (self.ca) {
    options.ca = self.ca
  }
  if (self.ciphers) {
    options.ciphers = self.ciphers
  }
  if (self.secureProtocol) {
    options.secureProtocol = self.secureProtocol
  }
  if (self.secureOptions) {
    options.secureOptions = self.secureOptions
  }
  if (typeof self.rejectUnauthorized !== 'undefined') {
    options.rejectUnauthorized = self.rejectUnauthorized
  }

  if (self.cert && self.key) {
    options.key = self.key
    options.cert = self.cert
  }

  if (self.pfx) {
    options.pfx = self.pfx
  }

  if (self.passphrase) {
    options.passphrase = self.passphrase
  }

  var poolKey = ''

  // different types of agents are in different pools
  if (Agent !== self.httpModule.Agent) {
    poolKey += Agent.name
  }

  // ca option is only relevant if proxy or destination are https
  var proxy = self.proxy
  if (typeof proxy === 'string') {
    proxy = url.parse(proxy)
  }
  var isHttps = (proxy && proxy.protocol === 'https:') || this.uri.protocol === 'https:'

  if (isHttps) {
    if (options.ca) {
      if (poolKey) {
        poolKey += ':'
      }
      poolKey += options.ca
    }

    if (typeof options.rejectUnauthorized !== 'undefined') {
      if (poolKey) {
        poolKey += ':'
      }
      poolKey += options.rejectUnauthorized
    }

    if (options.cert) {
      if (poolKey) {
        poolKey += ':'
      }
      poolKey += options.cert.toString('ascii') + options.key.toString('ascii')
    }

    if (options.pfx) {
      if (poolKey) {
        poolKey += ':'
      }
      poolKey += options.pfx.toString('ascii')
    }

    if (options.ciphers) {
      if (poolKey) {
        poolKey += ':'
      }
      poolKey += options.ciphers
    }

    if (options.secureProtocol) {
      if (poolKey) {
        poolKey += ':'
      }
      poolKey += options.secureProtocol
    }

    if (options.secureOptions) {
      if (poolKey) {
        poolKey += ':'
      }
      poolKey += options.secureOptions
    }
  }

  if (self.pool === globalPool && !poolKey && Object.keys(options).length === 0 && self.httpModule.globalAgent) {
    // not doing anything special.  Use the globalAgent
    return self.httpModule.globalAgent
  }

  // we're using a stored agent.  Make sure it's protocol-specific
  poolKey = self.uri.protocol + poolKey

  // generate a new agent for this setting if none yet exists
  if (!self.pool[poolKey]) {
    self.pool[poolKey] = new Agent(options)
    // properly set maxSockets on new agents
    if (self.pool.maxSockets) {
      self.pool[poolKey].maxSockets = self.pool.maxSockets
    }
  }

  return self.pool[poolKey]
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.hawk"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>hawk (opts)](#apidoc.element.request.Request.prototype.hawk)
- description and source-code
```javascript
hawk = function (opts) {
  var self = this
  self.setHeader('Authorization', hawk.client.header(self.uri, self.method, opts).field)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.httpSignature"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>httpSignature (opts)](#apidoc.element.request.Request.prototype.httpSignature)
- description and source-code
```javascript
httpSignature = function (opts) {
  var self = this
  httpSignature.signRequest({
    getHeader: function(header) {
      return self.getHeader(header, self.headers)
    },
    setHeader: function(header, value) {
      self.setHeader(header, value)
    },
    method: self.method,
    path: self.path
  }, opts)
  debug('httpSignature authorization', self.getHeader('authorization'))

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.init"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>init (options)](#apidoc.element.request.Request.prototype.init)
- description and source-code
```javascript
init = function (options) {
  // init() contains all the code to setup the request object.
  // the actual outgoing request is not started until start() is called
  // this function is called from both the constructor and on redirect.
  var self = this
  if (!options) {
    options = {}
  }
  self.headers = self.headers ? copy(self.headers) : {}

  // Delete headers with value undefined since they break
  // ClientRequest.OutgoingMessage.setHeader in node 0.12
  for (var headerName in self.headers) {
    if (typeof self.headers[headerName] === 'undefined') {
      delete self.headers[headerName]
    }
  }

  caseless.httpify(self, self.headers)

  if (!self.method) {
    self.method = options.method || 'GET'
  }
  if (!self.localAddress) {
    self.localAddress = options.localAddress
  }

  self._qs.init(options)

  debug(options)
  if (!self.pool && self.pool !== false) {
    self.pool = globalPool
  }
  self.dests = self.dests || []
  self.__isRequestRequest = true

  // Protect against double callback
  if (!self._callback && self.callback) {
    self._callback = self.callback
    self.callback = function () {
      if (self._callbackCalled) {
        return // Print a warning maybe?
      }
      self._callbackCalled = true
      self._callback.apply(self, arguments)
    }
    self.on('error', self.callback.bind())
    self.on('complete', self.callback.bind(self, null))
  }

  // People use this property instead all the time, so support it
  if (!self.uri && self.url) {
    self.uri = self.url
    delete self.url
  }

  // If there's a baseUrl, then use it as the base URL (i.e. uri must be
  // specified as a relative path and is appended to baseUrl).
  if (self.baseUrl) {
    if (typeof self.baseUrl !== 'string') {
      return self.emit('error', new Error('options.baseUrl must be a string'))
    }

    if (typeof self.uri !== 'string') {
      return self.emit('error', new Error('options.uri must be a string when using options.baseUrl'))
    }

    if (self.uri.indexOf('//') === 0 || self.uri.indexOf('://') !== -1) {
      return self.emit('error', new Error('options.uri must be a path when using options.baseUrl'))
    }

    // Handle all cases to make sure that there's only one slash between
    // baseUrl and uri.
    var baseUrlEndsWithSlash = self.baseUrl.lastIndexOf('/') === self.baseUrl.length - 1
    var uriStartsWithSlash = self.uri.indexOf('/') === 0

    if (baseUrlEndsWithSlash && uriStartsWithSlash) {
      self.uri = self.baseUrl + self.uri.slice(1)
    } else if (baseUrlEndsWithSlash || uriStartsWithSlash) {
      self.uri = self.baseUrl + self.uri
    } else if (self.uri === '') {
      self.uri = self.baseUrl
    } else {
      self.uri = self.baseUrl + '/' + self.uri
    }
    delete self.baseUrl
  }

  // A URI is needed by this point, emit error if we haven't been able to get one
  if (!self.uri) {
    return self.emit('error', new Error('options.uri is a required argument'))
  }

  // If a string URI/URL was given, parse it into a URL object
  if (typeof self.uri === 'string') {
    self.uri = url.parse(self.uri)
  }

  // Some URL objects are not from a URL parsed string and need href added
  if (!self.uri.href) {
    self.uri.href = url.format(self.uri)
  }

  // DEPRECATED: Warning for users of the old Unix Sockets URL Scheme
  if (self.uri.protocol === 'unix:') {
    return self.emit('error', new Error(''unix://' URL scheme is no longer supported. Please use the format 'http://unix:SOCKET:
PATH''))
  }

  // Support Unix Sockets
  if (self.uri.host === 'unix') {
    self.enableUnixSocket()
  }

  if (self.strictSSL === false) {
    self.rejectUnauthorized = false
  }

  if (!self.uri.pathname) {self.uri.pathname = '/'}

  if (!(self.uri.host || (self.uri.hostname && self.uri.port)) && !self.uri.isUnix) {
    // Invalid URI: it may generate lot of bad errors, like 'TypeError: Cannot call method 'indexOf' of undefined' in CookieJar
    // Detect and reject it as soon as possible
    var faultyUri = url.format(self.uri)
    var message = 'Invalid URI "' + faultyUri + '"'
    if (Object.keys(options). ...
```
- example usage
```shell
...

  if (!self.removeRefererHeader) {
    request.setHeader('referer', uriPrev.href)
  }

  request.emit('redirect')

  request.init()

  return true
}

exports.Redirect = Redirect
...
```

#### <a name="apidoc.element.request.Request.prototype.jar"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>jar (jar)](#apidoc.element.request.Request.prototype.jar)
- description and source-code
```javascript
jar = function (jar) {
  var self = this
  var cookies

  if (self._redirect.redirectsFollowed === 0) {
    self.originalCookieHeader = self.getHeader('cookie')
  }

  if (!jar) {
    // disable cookies
    cookies = false
    self._disableCookies = true
  } else {
    var targetCookieJar = (jar && jar.getCookieString) ? jar : globalCookieJar
    var urihref = self.uri.href
    //fetch cookie in the Specified host
    if (targetCookieJar) {
      cookies = targetCookieJar.getCookieString(urihref)
    }
  }

  //if need cookie and cookie is not empty
  if (cookies && cookies.length) {
    if (self.originalCookieHeader) {
      // Don't overwrite existing Cookie header
      self.setHeader('cookie', self.originalCookieHeader + '; ' + cookies)
    } else {
      self.setHeader('cookie', cookies)
    }
  }
  self._jar = jar
  return self
}
```
- example usage
```shell
...
### request.cookie

Function that creates a new cookie.

'''js
request.cookie('key1=value1')
'''
### request.jar()

Function that creates a new cookie jar.

'''js
request.jar()
'''
...
```

#### <a name="apidoc.element.request.Request.prototype.json"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>json (val)](#apidoc.element.request.Request.prototype.json)
- description and source-code
```javascript
json = function (val) {
  var self = this

  if (!self.hasHeader('accept')) {
    self.setHeader('accept', 'application/json')
  }

  if (typeof self.jsonReplacer === 'function') {
    self._jsonReplacer = self.jsonReplacer
  }

  self._json = true
  if (typeof val === 'boolean') {
    if (self.body !== undefined) {
      if (!/^application\/x-www-form-urlencoded\b/.test(self.getHeader('content-type'))) {
        self.body = safeStringify(self.body, self._jsonReplacer)
      } else {
        self.body = self._qs.rfc3986(self.body)
      }
      if (!self.hasHeader('content-type')) {
        self.setHeader('content-type', 'application/json')
      }
    }
  } else {
    self.body = safeStringify(val, self._jsonReplacer)
    if (!self.hasHeader('content-type')) {
      self.setHeader('content-type', 'application/json')
    }
  }

  if (typeof self.jsonReviver === 'function') {
    self._jsonReviver = self.jsonReviver
  }

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.multipart"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>multipart (multipart)](#apidoc.element.request.Request.prototype.multipart)
- description and source-code
```javascript
multipart = function (multipart) {
  var self = this

  self._multipart.onRequest(multipart)

  if (!self._multipart.chunked) {
    self.body = self._multipart.body
  }

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.oauth"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>oauth (_oauth)](#apidoc.element.request.Request.prototype.oauth)
- description and source-code
```javascript
oauth = function (_oauth) {
  var self = this

  self._oauth.onRequest(_oauth)

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.onRequestError"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>onRequestError (error)](#apidoc.element.request.Request.prototype.onRequestError)
- description and source-code
```javascript
onRequestError = function (error) {
  var self = this
  if (self._aborted) {
    return
  }
  if (self.req && self.req._reusedSocket && error.code === 'ECONNRESET'
      && self.agent.addRequestNoreuse) {
    self.agent = { addRequest: self.agent.addRequestNoreuse.bind(self.agent) }
    self.start()
    self.req.end()
    return
  }
  if (self.timeout && self.timeoutTimer) {
    clearTimeout(self.timeoutTimer)
    self.timeoutTimer = null
  }
  self.emit('error', error)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.onRequestResponse"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>onRequestResponse (response)](#apidoc.element.request.Request.prototype.onRequestResponse)
- description and source-code
```javascript
onRequestResponse = function (response) {
  var self = this

  if (self.timing) {
    self.timings.response = now() - self.startTimeNow
  }

  debug('onRequestResponse', self.uri.href, response.statusCode, response.headers)
  response.on('end', function() {
    if (self.timing) {
      self.timings.end = now() - self.startTimeNow
      response.timingStart = self.startTime

      // fill in the blanks for any periods that didn't trigger, such as
      // no lookup or connect due to keep alive
      if (!self.timings.socket) {
        self.timings.socket = 0
      }
      if (!self.timings.lookup) {
        self.timings.lookup = self.timings.socket
      }
      if (!self.timings.connect) {
        self.timings.connect = self.timings.lookup
      }
      if (!self.timings.response) {
        self.timings.response = self.timings.connect
      }

      debug('elapsed time', self.timings.end)

      // elapsedTime includes all redirects
      self.elapsedTime += Math.round(self.timings.end)

      // NOTE: elapsedTime is deprecated in favor of .timings
      response.elapsedTime = self.elapsedTime

      // timings is just for the final fetch
      response.timings = self.timings

      // pre-calculate phase timings as well
      response.timingPhases = {
        wait: self.timings.socket,
        dns: self.timings.lookup - self.timings.socket,
        tcp: self.timings.connect - self.timings.lookup,
        firstByte: self.timings.response - self.timings.connect,
        download: self.timings.end - self.timings.response,
        total: self.timings.end
      }
    }
    debug('response end', self.uri.href, response.statusCode, response.headers)
  })

  if (self._aborted) {
    debug('aborted', self.uri.href)
    response.resume()
    return
  }

  self.response = response
  response.request = self
  response.toJSON = responseToJSON

  // XXX This is different on 0.10, because SSL is strict by default
  if (self.httpModule === https &&
      self.strictSSL && (!response.hasOwnProperty('socket') ||
      !response.socket.authorized)) {
    debug('strict ssl error', self.uri.href)
    var sslErr = response.hasOwnProperty('socket') ? response.socket.authorizationError : self.uri.href + ' does not support SSL
'
    self.emit('error', new Error('SSL Error: ' + sslErr))
    return
  }

  // Save the original host before any redirect (if it changes, we need to
  // remove any authorization headers).  Also remember the case of the header
  // name because lots of broken servers expect Host instead of host and we
  // want the caller to be able to specify this.
  self.originalHost = self.getHeader('host')
  if (!self.originalHostHeaderName) {
    self.originalHostHeaderName = self.hasHeader('host')
  }
  if (self.setHost) {
    self.removeHeader('host')
  }
  if (self.timeout && self.timeoutTimer) {
    clearTimeout(self.timeoutTimer)
    self.timeoutTimer = null
  }

  var targetCookieJar = (self._jar && self._jar.setCookie) ? self._jar : globalCookieJar
  var addCookie = function (cookie) {
    //set the cookie if it's domain in the href's domain.
    try {
      targetCookieJar.setCookie(cookie, self.uri.href, {ignoreError: true})
    } catch (e) {
      self.emit('error', e)
    }
  }

  response.caseless = caseless(response.headers)

  if (response.caseless.has('set-cookie') && (!self._disableCookies)) {
    var headerName = response.caseless.has('set-cookie')
    if (Array.isArray(response.headers[headerName])) {
      response.headers[headerName].forEach(addCookie)
    } else {
      addCookie(response.headers[headerName])
    }
  }

  if (self._redirect.onResponse(response)) {
    return // Ignore the rest of the response
  } else {
    // Be a good stream and emit end when the response is finished.
    // Hack to emit end on close because of a core bug that never fires end
    response.on('close', function () {
      if (!self._ended) {
        self.response.emit('end')
      }
    })

    response.once('end', function () {
      self._ended = true
    })

    var noBody = function (code) {
      return (
        self.method === 'HEAD' ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.pause"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>pause ()](#apidoc.element.request.Request.prototype.pause)
- description and source-code
```javascript
pause = function () {
  var self = this
  if (!self.responseContent) {
    self._paused = true
  } else {
    self.responseContent.pause.apply(self.responseContent, arguments)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.pipe"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>pipe (dest, opts)](#apidoc.element.request.Request.prototype.pipe)
- description and source-code
```javascript
pipe = function (dest, opts) {
  var self = this

  if (self.response) {
    if (self._destdata) {
      self.emit('error', new Error('You cannot pipe after data has been emitted from the response.'))
    } else if (self._ended) {
      self.emit('error', new Error('You cannot pipe after the response has been ended.'))
    } else {
      stream.Stream.prototype.pipe.call(self, dest, opts)
      self.pipeDest(dest)
      return dest
    }
  } else {
    self.dests.push(dest)
    stream.Stream.prototype.pipe.call(self, dest, opts)
    return dest
  }
}
```
- example usage
```shell
...


## Streaming

You can stream any response to a file stream.

'''js
request('http://google.com/doodle.png').pipe(fs.createWriteStream('doodle.png'))
'''

You can also stream a file to a PUT or POST request. This method will also check the file extension against a mapping of file extensions
 to content-types (in this case 'application/json') and use the proper 'content-type' in the PUT request (if the headers don’t already
 provide one).

'''js
fs.createReadStream('file.json').pipe(request.put('http://mysite.com/obj.json'))
'''
...
```

#### <a name="apidoc.element.request.Request.prototype.pipeDest"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>pipeDest (dest)](#apidoc.element.request.Request.prototype.pipeDest)
- description and source-code
```javascript
pipeDest = function (dest) {
  var self = this
  var response = self.response
  // Called after the response is received
  if (dest.headers && !dest.headersSent) {
    if (response.caseless.has('content-type')) {
      var ctname = response.caseless.has('content-type')
      if (dest.setHeader) {
        dest.setHeader(ctname, response.headers[ctname])
      }
      else {
        dest.headers[ctname] = response.headers[ctname]
      }
    }

    if (response.caseless.has('content-length')) {
      var clname = response.caseless.has('content-length')
      if (dest.setHeader) {
        dest.setHeader(clname, response.headers[clname])
      } else {
        dest.headers[clname] = response.headers[clname]
      }
    }
  }
  if (dest.setHeader && !dest.headersSent) {
    for (var i in response.headers) {
      // If the response content is being decoded, the Content-Encoding header
      // of the response doesn't represent the piped content, so don't pass it.
      if (!self.gzip || i !== 'content-encoding') {
        dest.setHeader(i, response.headers[i])
      }
    }
    dest.statusCode = response.statusCode
  }
  if (self.pipefilter) {
    self.pipefilter(response, dest)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.qs"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>qs (q, clobber)](#apidoc.element.request.Request.prototype.qs)
- description and source-code
```javascript
qs = function (q, clobber) {
  var self = this
  var base
  if (!clobber && self.uri.query) {
    base = self._qs.parse(self.uri.query)
  } else {
    base = {}
  }

  for (var i in q) {
    base[i] = q[i]
  }

  var qs = self._qs.stringify(base)

  if (qs === '') {
    return self
  }

  self.uri = url.parse(self.uri.href.split('?')[0] + '?' + qs)
  self.url = self.uri
  self.path = self.uri.path

  if (self.uri.host === 'unix') {
    self.enableUnixSocket()
  }

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.readResponseBody"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>readResponseBody (response)](#apidoc.element.request.Request.prototype.readResponseBody)
- description and source-code
```javascript
readResponseBody = function (response) {
  var self = this
  debug('reading response\'s body')
  var buffers = []
    , bufferLength = 0
    , strings = []

  self.on('data', function (chunk) {
    if (!Buffer.isBuffer(chunk)) {
      strings.push(chunk)
    } else if (chunk.length) {
      bufferLength += chunk.length
      buffers.push(chunk)
    }
  })
  self.on('end', function () {
    debug('end event', self.uri.href)
    if (self._aborted) {
      debug('aborted', self.uri.href)
      // 'buffer' is defined in the parent scope and used in a closure it exists for the life of the request.
      // This can lead to leaky behavior if the user retains a reference to the request object.
      buffers = []
      bufferLength = 0
      return
    }

    if (bufferLength) {
      debug('has body', self.uri.href, bufferLength)
      response.body = Buffer.concat(buffers, bufferLength)
      if (self.encoding !== null) {
        response.body = response.body.toString(self.encoding)
      }
      // 'buffer' is defined in the parent scope and used in a closure it exists for the life of the Request.
      // This can lead to leaky behavior if the user retains a reference to the request object.
      buffers = []
      bufferLength = 0
    } else if (strings.length) {
      // The UTF8 BOM [0xEF,0xBB,0xBF] is converted to [0xFE,0xFF] in the JS UTC16/UCS2 representation.
      // Strip this value out when the encoding is set to 'utf8', as upstream consumers won't expect it and it breaks JSON.parse
().
      if (self.encoding === 'utf8' && strings[0].length > 0 && strings[0][0] === '\uFEFF') {
        strings[0] = strings[0].substring(1)
      }
      response.body = strings.join('')
    }

    if (self._json) {
      try {
        response.body = JSON.parse(response.body, self._jsonReviver)
      } catch (e) {
        debug('invalid JSON received', self.uri.href)
      }
    }
    debug('emitting complete', self.uri.href)
    if (typeof response.body === 'undefined' && !self._json) {
      response.body = self.encoding === null ? Buffer.alloc(0) : ''
    }
    self.emit('complete', response, response.body)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.resume"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>resume ()](#apidoc.element.request.Request.prototype.resume)
- description and source-code
```javascript
resume = function () {
  var self = this
  if (!self.responseContent) {
    self._paused = false
  } else {
    self.responseContent.resume.apply(self.responseContent, arguments)
  }
}
```
- example usage
```shell
...

request.debug('redirect to', redirectTo)

// ignore any potential response body.  it cannot possibly be useful
// to us at this point.
// response.resume should be defined, but check anyway before calling. Workaround for browserify.
if (response.resume) {
  response.resume()
}

if (self.redirectsFollowed >= self.maxRedirects) {
  request.emit('error', new Error('Exceeded maxRedirects. Probably stuck in a redirect loop ' + request.uri.href))
  return false
}
self.redirectsFollowed += 1
...
```

#### <a name="apidoc.element.request.Request.prototype.start"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>start ()](#apidoc.element.request.Request.prototype.start)
- description and source-code
```javascript
start = function () {
  // start() is called once we are ready to send the outgoing HTTP request.
  // this is usually called on the first write(), end() or on nextTick()
  var self = this

  if (self.timing) {
    // All timings will be relative to this request's startTime.  In order to do this,
    // we need to capture the wall-clock start time (via Date), immediately followed
    // by the high-resolution timer (via now()).  While these two won't be set
    // at the _exact_ same time, they should be close enough to be able to calculate
    // high-resolution, monotonically non-decreasing timestamps relative to startTime.
    var startTime = new Date().getTime()
    var startTimeNow = now()
  }

  if (self._aborted) {
    return
  }

  self._started = true
  self.method = self.method || 'GET'
  self.href = self.uri.href

  if (self.src && self.src.stat && self.src.stat.size && !self.hasHeader('content-length')) {
    self.setHeader('content-length', self.src.stat.size)
  }
  if (self._aws) {
    self.aws(self._aws, true)
  }

  // We have a method named auth, which is completely different from the http.request
  // auth option.  If we don't remove it, we're gonna have a bad time.
  var reqOptions = copy(self)
  delete reqOptions.auth

  debug('make request', self.uri.href)

  // node v6.8.0 now supports a 'timeout' value in 'http.request()', but we
  // should delete it for now since we handle timeouts manually for better
  // consistency with node versions before v6.8.0
  delete reqOptions.timeout

  try {
    self.req = self.httpModule.request(reqOptions)
  } catch (err) {
    self.emit('error', err)
    return
  }

  if (self.timing) {
    self.startTime = startTime
    self.startTimeNow = startTimeNow

    // Timing values will all be relative to startTime (by comparing to startTimeNow
    // so we have an accurate clock)
    self.timings = {}
  }

  var timeout
  if (self.timeout && !self.timeoutTimer) {
    if (self.timeout < 0) {
      timeout = 0
    } else if (typeof self.timeout === 'number' && isFinite(self.timeout)) {
      timeout = self.timeout
    }
  }

  self.req.on('response', self.onRequestResponse.bind(self))
  self.req.on('error', self.onRequestError.bind(self))
  self.req.on('drain', function() {
    self.emit('drain')
  })
  self.req.on('socket', function(socket) {
    // '._connecting' was the old property which was made public in node v6.1.0
    var isConnecting = socket._connecting || socket.connecting
    if (self.timing) {
      self.timings.socket = now() - self.startTimeNow

      if (isConnecting) {
        var onLookupTiming = function() {
          self.timings.lookup = now() - self.startTimeNow
        }

        var onConnectTiming = function() {
          self.timings.connect = now() - self.startTimeNow
        }

        socket.once('lookup', onLookupTiming)
        socket.once('connect', onConnectTiming)

        // clean up timing event listeners if needed on error
        self.req.once('error', function() {
          socket.removeListener('lookup', onLookupTiming)
          socket.removeListener('connect', onConnectTiming)
        })
      }
    }

    var setReqTimeout = function() {
      // This timeout sets the amount of time to wait *between* bytes sent
      // from the server once connected.
      //
      // In particular, it's useful for erroring if the server fails to send
      // data halfway through streaming a response.
      self.req.setTimeout(timeout, function () {
        if (self.req) {
          self.abort()
          var e = new Error('ESOCKETTIMEDOUT')
          e.code = 'ESOCKETTIMEDOUT'
          e.connect = false
          self.emit('error', e)
        }
      })
    }
    if (timeout !== undefined) {
      // Only start the connection timer if we're actually connecting a new
      // socket, otherwise if we're already connected (because this is a
      // keep-alive connection) do not bother. This is important since we won't
      // get a 'connect' event for an already connected socket.
      if (isConnecting) {
        var onReqSockConnect = function() { ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>toJSON ()](#apidoc.element.request.Request.prototype.toJSON)
- description and source-code
```javascript
function requestToJSON() {
  var self = this
  return {
    uri: self.uri,
    method: self.method,
    headers: self.headers
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.Request.prototype.write"></a>[function <span class="apidocSignatureSpan">request.Request.prototype.</span>write ()](#apidoc.element.request.Request.prototype.write)
- description and source-code
```javascript
write = function () {
  var self = this
  if (self._aborted) {return}

  if (!self._started) {
    self.start()
  }
  if (self.req) {
    return self.req.write.apply(self.req, arguments)
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.auth"></a>[module request.auth](#apidoc.module.request.auth)

#### <a name="apidoc.element.request.auth.Auth"></a>[function <span class="apidocSignatureSpan">request.auth.</span>Auth (request)](#apidoc.element.request.auth.Auth)
- description and source-code
```javascript
function Auth(request) {
  // define all public properties here
  this.request = request
  this.hasAuth = false
  this.sentAuth = false
  this.bearerToken = null
  this.user = null
  this.pass = null
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.cookies"></a>[module request.cookies](#apidoc.module.request.cookies)

#### <a name="apidoc.element.request.cookies.jar"></a>[function <span class="apidocSignatureSpan">request.cookies.</span>jar (store)](#apidoc.element.request.cookies.jar)
- description and source-code
```javascript
jar = function (store) {
  return new RequestJar(store)
}
```
- example usage
```shell
...
### request.cookie

Function that creates a new cookie.

'''js
request.cookie('key1=value1')
'''
### request.jar()

Function that creates a new cookie jar.

'''js
request.jar()
'''
...
```

#### <a name="apidoc.element.request.cookies.parse"></a>[function <span class="apidocSignatureSpan">request.cookies.</span>parse (str)](#apidoc.element.request.cookies.parse)
- description and source-code
```javascript
parse = function (str) {
  if (str && str.uri) {
    str = str.uri
  }
  if (typeof str !== 'string') {
    throw new Error('The cookie function only accepts STRING as param')
  }
  return Cookie.parse(str, {loose: true})
}
```
- example usage
```shell
...
  headers: {
    'User-Agent': 'request'
  }
};

function callback(error, response, body) {
  if (!error && response.statusCode == 200) {
    var info = JSON.parse(body);
    console.log(info.stargazers_count + " Stars");
    console.log(info.forks_count + " Forks");
  }
}

request(options, callback);
'''
...
```



# <a name="apidoc.module.request.har"></a>[module request.har](#apidoc.module.request.har)

#### <a name="apidoc.element.request.har.Har"></a>[function <span class="apidocSignatureSpan">request.har.</span>Har (request)](#apidoc.element.request.har.Har)
- description and source-code
```javascript
function Har(request) {
  this.request = request
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.helpers"></a>[module request.helpers](#apidoc.module.request.helpers)

#### <a name="apidoc.element.request.helpers.copy"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>copy (obj)](#apidoc.element.request.helpers.copy)
- description and source-code
```javascript
function copy(obj) {
  var o = {}
  Object.keys(obj).forEach(function (i) {
    o[i] = obj[i]
  })
  return o
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.helpers.defer"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>defer (callback, arg1, arg2, arg3)](#apidoc.element.request.helpers.defer)
- description and source-code
```javascript
defer = function (callback, arg1, arg2, arg3) {
  if (typeof callback !== 'function') {
    throw new TypeError('"callback" argument must be a function');
  }

  var i, args;

  switch (arguments.length) {
    // fast cases
    case 1:
      break;
    case 2:
      args = [arg1];
      break;
    case 3:
      args = [arg1, arg2];
      break;
    default:
      args = [arg1, arg2, arg3];
      for (i = 4; i < arguments.length; i++)
        // extend array dynamically, makes .apply run much faster in v6.0.0
        args[i - 1] = arguments[i];
      break;
  }
  return createImmediate(args, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.helpers.isReadStream"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>isReadStream (rs)](#apidoc.element.request.helpers.isReadStream)
- description and source-code
```javascript
function isReadStream(rs) {
  return rs.readable && rs.path && rs.mode
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.helpers.md5"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>md5 (str)](#apidoc.element.request.helpers.md5)
- description and source-code
```javascript
function md5(str) {
  return crypto.createHash('md5').update(str).digest('hex')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.helpers.paramsHaveRequestBody"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>paramsHaveRequestBody (params)](#apidoc.element.request.helpers.paramsHaveRequestBody)
- description and source-code
```javascript
function paramsHaveRequestBody(params) {
  return (
    params.body ||
    params.requestBodyStream ||
    (params.json && typeof params.json !== 'boolean') ||
    params.multipart
  )
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.helpers.safeStringify"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>safeStringify (obj, replacer)](#apidoc.element.request.helpers.safeStringify)
- description and source-code
```javascript
function safeStringify(obj, replacer) {
  var ret
  try {
    ret = JSON.stringify(obj, replacer)
  } catch (e) {
    ret = jsonSafeStringify(obj, replacer)
  }
  return ret
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.helpers.toBase64"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>toBase64 (str)](#apidoc.element.request.helpers.toBase64)
- description and source-code
```javascript
function toBase64(str) {
  return Buffer.from(str || '', 'utf8').toString('base64')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.request.helpers.version"></a>[function <span class="apidocSignatureSpan">request.helpers.</span>version ()](#apidoc.element.request.helpers.version)
- description and source-code
```javascript
function version() {
  var numbers = process.version.replace('v', '').split('.')
  return {
    major: parseInt(numbers[0], 10),
    minor: parseInt(numbers[1], 10),
    patch: parseInt(numbers[2], 10)
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.multipart"></a>[module request.multipart](#apidoc.module.request.multipart)

#### <a name="apidoc.element.request.multipart.Multipart"></a>[function <span class="apidocSignatureSpan">request.multipart.</span>Multipart (request)](#apidoc.element.request.multipart.Multipart)
- description and source-code
```javascript
function Multipart(request) {
  this.request = request
  this.boundary = uuid()
  this.chunked = false
  this.body = null
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.oauth"></a>[module request.oauth](#apidoc.module.request.oauth)

#### <a name="apidoc.element.request.oauth.OAuth"></a>[function <span class="apidocSignatureSpan">request.oauth.</span>OAuth (request)](#apidoc.element.request.oauth.OAuth)
- description and source-code
```javascript
function OAuth(request) {
  this.request = request
  this.params = null
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.querystring"></a>[module request.querystring](#apidoc.module.request.querystring)

#### <a name="apidoc.element.request.querystring.Querystring"></a>[function <span class="apidocSignatureSpan">request.querystring.</span>Querystring (request)](#apidoc.element.request.querystring.Querystring)
- description and source-code
```javascript
function Querystring(request) {
  this.request = request
  this.lib = null
  this.useQuerystring = null
  this.parseOptions = null
  this.stringifyOptions = null
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.redirect"></a>[module request.redirect](#apidoc.module.request.redirect)

#### <a name="apidoc.element.request.redirect.Redirect"></a>[function <span class="apidocSignatureSpan">request.redirect.</span>Redirect (request)](#apidoc.element.request.redirect.Redirect)
- description and source-code
```javascript
function Redirect(request) {
  this.request = request
  this.followRedirect = true
  this.followRedirects = true
  this.followAllRedirects = false
  this.followOriginalHttpMethod = false
  this.allowRedirect = function () {return true}
  this.maxRedirects = 10
  this.redirects = []
  this.redirectsFollowed = 0
  this.removeRefererHeader = false
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.request.tunnel"></a>[module request.tunnel](#apidoc.module.request.tunnel)

#### <a name="apidoc.element.request.tunnel.Tunnel"></a>[function <span class="apidocSignatureSpan">request.tunnel.</span>Tunnel (request)](#apidoc.element.request.tunnel.Tunnel)
- description and source-code
```javascript
function Tunnel(request) {
  this.request = request
  this.proxyHeaderWhiteList = defaultProxyHeaderWhiteList
  this.proxyHeaderExclusiveList = []
  if (typeof request.tunnel !== 'undefined') {
    this.tunnelOverride = request.tunnel
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
