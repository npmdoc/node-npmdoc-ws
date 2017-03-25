# api documentation for  [ws (v2.2.2)](https://github.com/websockets/ws#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ws.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ws)
#### Simple to use, blazing fast and thoroughly tested websocket client and server for Node.js

[![NPM](https://nodei.co/npm/ws.png?downloads=true)](https://www.npmjs.com/package/ws)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ws/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ws_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ws/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-ws/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Einar Otto Stangvik",
        "email": "einaros@gmail.com",
        "url": "http://2x.io"
    },
    "bugs": {
        "url": "https://github.com/websockets/ws/issues"
    },
    "dependencies": {
        "ultron": "~1.1.0"
    },
    "description": "Simple to use, blazing fast and thoroughly tested websocket client and server for Node.js",
    "devDependencies": {
        "benchmark": "~2.1.2",
        "bufferutil": "~3.0.0",
        "eslint": "~3.18.0",
        "eslint-config-standard": "~8.0.0-beta.1",
        "eslint-plugin-import": "~2.2.0",
        "eslint-plugin-node": "~4.2.0",
        "eslint-plugin-promise": "~3.5.0",
        "eslint-plugin-standard": "~2.1.0",
        "istanbul": "~0.4.5",
        "mocha": "~3.2.0",
        "utf-8-validate": "~3.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "aa26daf39c52b20ed716e3447f8641494a726b01",
        "tarball": "https://registry.npmjs.org/ws/-/ws-2.2.2.tgz"
    },
    "gitHead": "286d513c1239bc2f1c9d23d997de1c954d3c8615",
    "homepage": "https://github.com/websockets/ws#readme",
    "keywords": [
        "HyBi",
        "Push",
        "RFC-6455",
        "WebSocket",
        "WebSockets",
        "real-time"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "3rdeden",
            "email": "npm@3rd-Eden.com"
        },
        {
            "name": "einaros",
            "email": "einaros@gmail.com"
        },
        {
            "name": "lpinca",
            "email": "luigipinca@gmail.com"
        },
        {
            "name": "v1",
            "email": "npm@3rd-Eden.com"
        }
    ],
    "name": "ws",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/websockets/ws.git"
    },
    "scripts": {
        "coverage": "istanbul cover _mocha --report html -- test/*.test.js",
        "integration": "npm run lint && mocha test/*.integration.js",
        "lint": "eslint .",
        "test": "npm run lint && mocha test/*.test.js",
        "test-travis": "npm run lint && istanbul cover _mocha --report lcovonly -- test/*.test.js"
    },
    "version": "2.2.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ws](#apidoc.module.ws)
1.  [function <span class="apidocSignatureSpan">ws.</span>Receiver (extensions, maxPayload, binaryType)](#apidoc.element.ws.Receiver)
1.  [function <span class="apidocSignatureSpan">ws.</span>Sender (socket, extensions)](#apidoc.element.ws.Sender)
1.  [function <span class="apidocSignatureSpan">ws.</span>Server (Boolean|Object)](#apidoc.element.ws.Server)
1.  number <span class="apidocSignatureSpan">ws.</span>CLOSED
1.  number <span class="apidocSignatureSpan">ws.</span>CLOSING
1.  number <span class="apidocSignatureSpan">ws.</span>CONNECTING
1.  number <span class="apidocSignatureSpan">ws.</span>OPEN
1.  object <span class="apidocSignatureSpan">ws.</span>BufferUtil
1.  object <span class="apidocSignatureSpan">ws.</span>Constants
1.  object <span class="apidocSignatureSpan">ws.</span>ErrorCodes
1.  object <span class="apidocSignatureSpan">ws.</span>EventTarget
1.  object <span class="apidocSignatureSpan">ws.</span>Extensions

#### [module ws.BufferUtil](#apidoc.module.ws.BufferUtil)
1.  [function <span class="apidocSignatureSpan">ws.BufferUtil.</span>concat (list, totalLength)](#apidoc.element.ws.BufferUtil.concat)
1.  [function <span class="apidocSignatureSpan">ws.BufferUtil.</span>mask (source, mask, output, offset, length)](#apidoc.element.ws.BufferUtil.mask)
1.  [function <span class="apidocSignatureSpan">ws.BufferUtil.</span>unmask (buffer, mask)](#apidoc.element.ws.BufferUtil.unmask)

#### [module ws.Constants](#apidoc.module.ws.Constants)
1.  [function <span class="apidocSignatureSpan">ws.Constants.</span>NOOP ()](#apidoc.element.ws.Constants.NOOP)
1.  object <span class="apidocSignatureSpan">ws.Constants.</span>BINARY_TYPES
1.  object <span class="apidocSignatureSpan">ws.Constants.</span>EMPTY_BUFFER
1.  string <span class="apidocSignatureSpan">ws.Constants.</span>GUID

#### [module ws.ErrorCodes](#apidoc.module.ws.ErrorCodes)
1.  [function <span class="apidocSignatureSpan">ws.ErrorCodes.</span>isValidErrorCode (code)](#apidoc.element.ws.ErrorCodes.isValidErrorCode)
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1000
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1001
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1002
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1003
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1004
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1005
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1006
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1007
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1008
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1009
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1010
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1011
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1012
1.  string <span class="apidocSignatureSpan">ws.ErrorCodes.</span>1013

#### [module ws.EventTarget](#apidoc.module.ws.EventTarget)
1.  [function <span class="apidocSignatureSpan">ws.EventTarget.</span>addEventListener (method, listener)](#apidoc.element.ws.EventTarget.addEventListener)
1.  [function <span class="apidocSignatureSpan">ws.EventTarget.</span>removeEventListener (method, listener)](#apidoc.element.ws.EventTarget.removeEventListener)

#### [module ws.Extensions](#apidoc.module.ws.Extensions)
1.  [function <span class="apidocSignatureSpan">ws.Extensions.</span>format (value)](#apidoc.element.ws.Extensions.format)
1.  [function <span class="apidocSignatureSpan">ws.Extensions.</span>parse (value)](#apidoc.element.ws.Extensions.parse)



# <a name="apidoc.module.ws"></a>[module ws](#apidoc.module.ws)

#### <a name="apidoc.element.ws.Receiver"></a>[function <span class="apidocSignatureSpan">ws.</span>Receiver (extensions, maxPayload, binaryType)](#apidoc.element.ws.Receiver)
- description and source-code
```javascript
class Receiver {
<span class="apidocCodeCommentSpan">  /**
   * Creates a Receiver instance.
   *
   * @param {Object} extensions An object containing the negotiated extensions
   * @param {Number} maxPayload The maximum allowed message length
   * @param {String} binaryType The type for binary data
   */
</span>  constructor (extensions, maxPayload, binaryType) {
    this.binaryType = binaryType || constants.BINARY_TYPES[0];
    this.extensions = extensions || {};
    this.maxPayload = maxPayload | 0;

    this.bufferedBytes = 0;
    this.buffers = [];

    this.compressed = false;
    this.payloadLength = 0;
    this.fragmented = 0;
    this.masked = false;
    this.fin = false;
    this.mask = null;
    this.opcode = 0;

    this.totalPayloadLength = 0;
    this.messageLength = 0;
    this.fragments = [];

    this.cleanupCallback = null;
    this.hadError = false;
    this.dead = false;
    this.loop = false;

    this.onmessage = null;
    this.onclose = null;
    this.onerror = null;
    this.onping = null;
    this.onpong = null;

    this.state = GET_INFO;
  }

  /**
   * Consumes bytes from the available buffered data.
   *
   * @param {Number} bytes The number of bytes to consume
   * @return {Buffer} Consumed bytes
   * @private
   */
  readBuffer (bytes) {
    var offset = 0;
    var dst;
    var l;

    this.bufferedBytes -= bytes;

    if (bytes === this.buffers[0].length) return this.buffers.shift();

    if (bytes < this.buffers[0].length) {
      dst = this.buffers[0].slice(0, bytes);
      this.buffers[0] = this.buffers[0].slice(bytes);
      return dst;
    }

    dst = Buffer.allocUnsafe(bytes);

    while (bytes > 0) {
      l = this.buffers[0].length;

      if (bytes >= l) {
        this.buffers[0].copy(dst, offset);
        offset += l;
        this.buffers.shift();
      } else {
        this.buffers[0].copy(dst, offset, 0, bytes);
        this.buffers[0] = this.buffers[0].slice(bytes);
      }

      bytes -= l;
    }

    return dst;
  }

  /**
   * Checks if the number of buffered bytes is bigger or equal than 'n' and
   * calls 'cleanup' if necessary.
   *
   * @param {Number} n The number of bytes to check against
   * @return {Boolean} 'true' if 'bufferedBytes >= n', else 'false'
   * @private
   */
  hasBufferedBytes (n) {
    if (this.bufferedBytes >= n) return true;

    this.loop = false;
    if (this.dead) this.cleanup(this.cleanupCallback);
    return false;
  }

  /**
   * Adds new data to the parser.
   *
   * @public
   */
  add (data) {
    if (this.dead) return;

    this.bufferedBytes += data.length;
    this.buffers.push(data);
    this.startLoop();
  }

  /**
   * Starts the parsing loop.
   *
   * @private
   */
  startLoop () {
    this.loop = true;

    while (this.loop) {
      switch (this.state) {
        case GET_INFO:
          this.getInfo();
          break;
        case GET_PAYLOAD_LENGTH_16:
          this.getPayloadLength16();
          break;
        case GET_PAYLOAD_LENGTH_64:
          this.getPayloadLength64();
          break;
        case GET_MASK:
          this.getMask();
          break;
        case GET_DATA:
          this.getData();
          break;
        default: // 'INFLATING'
          this.loop = false;
      }
    }
  }

  /**
   * Reads the first two bytes of a frame.
   *
   * @private
   */
  getInfo () {
    if (!this.hasBufferedBytes(2)) return;

    const buf = this.readBuffer(2);

    if ((buf[0] & 0x30) !== 0x00) {
      this.error(new Error('RSV2 and RSV3 must be clear'), 1002);
      return;
    }

    const compressed = (buf[0] & 0x40) === 0x40;

    if (compressed && !this.extensions[PerMessageDeflate.extensionName]) {
      this.error(new Error('RSV1 must be clear'), 1002);
      return;
    }

    this.fin = (buf[0] & 0x80) === 0x80;
    this.opcode = buf[0] & 0x0f;
    this.payloadLength = buf[1] & 0x7f;

    if (this.opcode === 0x00) {
      if (compressed) {
        this.error(new Error('RSV1 must be clear'), 1002);
        return;
      }

      if (!this.fragmented) {
        this.error(new Error('invalid opcode: ${this.opcode}'), 1002);
        return;
      } else { ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ws.Sender"></a>[function <span class="apidocSignatureSpan">ws.</span>Sender (socket, extensions)](#apidoc.element.ws.Sender)
- description and source-code
```javascript
class Sender {
<span class="apidocCodeCommentSpan">  /**
   * Creates a Sender instance.
   *
   * @param {net.Socket} socket The connection socket
   * @param {Object} extensions An object containing the negotiated extensions
   */
</span>  constructor (socket, extensions) {
    this.perMessageDeflate = (extensions || {})[PerMessageDeflate.extensionName];
    this._socket = socket;

    this.firstFragment = true;
    this.compress = false;

    this.bufferedBytes = 0;
    this.deflating = false;
    this.queue = [];

    this.onerror = null;
  }

  /**
   * Frames a piece of data according to the HyBi WebSocket protocol.
   *
   * @param {Buffer} data The data to frame
   * @param {Object} options Options object
   * @param {Number} options.opcode The opcode
   * @param {Boolean} options.readOnly Specifies whether 'data' can be modified
   * @param {Boolean} options.fin Specifies whether or not to set the FIN bit
   * @param {Boolean} options.mask Specifies whether or not to mask 'data'
   * @param {Boolean} options.rsv1 Specifies whether or not to set the RSV1 bit
   * @return {Buffer[]} The framed data as a list of 'Buffer' instances
   * @public
   */
  static frame (data, options) {
    const merge = data.length < 1024 || (options.mask && options.readOnly);
    var offset = options.mask ? 6 : 2;
    var payloadLength = data.length;

    if (data.length >= 65536) {
      offset += 8;
      payloadLength = 127;
    } else if (data.length > 125) {
      offset += 2;
      payloadLength = 126;
    }

    const target = Buffer.allocUnsafe(merge ? data.length + offset : offset);

    target[0] = options.fin ? options.opcode | 0x80 : options.opcode;
    if (options.rsv1) target[0] |= 0x40;

    if (payloadLength === 126) {
      target.writeUInt16BE(data.length, 2, true);
    } else if (payloadLength === 127) {
      target.writeUInt32BE(0, 2, true);
      target.writeUInt32BE(data.length, 6, true);
    }

    if (!options.mask) {
      target[1] = payloadLength;
      if (merge) {
        data.copy(target, offset);
        return [target];
      }

      return [target, data];
    }

    const mask = crypto.randomBytes(4);

    target[1] = payloadLength | 0x80;
    target[offset - 4] = mask[0];
    target[offset - 3] = mask[1];
    target[offset - 2] = mask[2];
    target[offset - 1] = mask[3];

    if (merge) {
      bufferUtil.mask(data, mask, target, offset, data.length);
      return [target];
    }

    bufferUtil.mask(data, mask, data, 0, data.length);
    return [target, data];
  }

  /**
   * Sends a close message to the other peer.
   *
   * @param {(Number|undefined)} code The status code component of the body
   * @param {String} data The message component of the body
   * @param {Boolean} mask Specifies whether or not to mask the message
   * @param {Function} cb Callback
   * @public
   */
  close (code, data, mask, cb) {
    if (code !== undefined && (typeof code !== 'number' || !ErrorCodes.isValidErrorCode(code))) {
      throw new Error('first argument must be a valid error code number');
    }

    const buf = Buffer.allocUnsafe(2 + (data ? Buffer.byteLength(data) : 0));

    buf.writeUInt16BE(code || 1000, 0, true);
    if (buf.length > 2) buf.write(data, 2);

    if (this.deflating) {
      this.enqueue([this.doClose, buf, mask, cb]);
    } else {
      this.doClose(buf, mask, cb);
    }
  }

  /**
   * Frames and sends a close message.
   *
   * @param {Buffer} data The message to send
   * @param {Boolean} mask Specifies whether or not to mask 'data'
   * @param {Function} cb Callback
   * @private
   */
  doClose (data, mask, cb) {
    this.sendFrame(Sender.frame(data, {
      readOnly: false,
      opcode: 0x08,
      rsv1: false,
      fin: true,
      mask
    }), cb);
  }

  /**
   * Sends a ping message to the other peer.
   *
   * @param {*} data The message to send
   * @param {Boolean} mask Specifies whether or not to mask 'data'
   * @public
   */
  ping (data, mask) {
    var readOnly = true;

    if (!Buffer.isBuffer(data)) {
      if (data instanceof ArrayBuffer) {
        data = Buffer.from(data);
      } else if (ArrayBuffer.isV ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ws.Server"></a>[function <span class="apidocSignatureSpan">ws.</span>Server (Boolean|Object)](#apidoc.element.ws.Server)
- description and source-code
```javascript
class WebSocketServer extends EventEmitter {
<span class="apidocCodeCommentSpan">  /**
   * Create a 'WebSocketServer' instance.
   *
   * @param {Object} options Configuration options
   * @param {String} options.host The hostname where to bind the server
   * @param {Number} options.port The port where to bind the server
   * @param {http.Server} options.server A pre-created HTTP/S server to use
   * @param {Function} options.verifyClient An hook to reject connections
   * @param {Function} options.handleProtocols An hook to handle protocols
   * @param {String} options.path Accept only connections matching this path
   * @param {Boolean} options.noServer Enable no server mode
   * @param {Boolean} options.clientTracking Specifies whether or not to track clients
   * @param {(Boolean|Object)} options.perMessageDeflate Enable/disable permessage-deflate
   * @param {Number} options.maxPayload The maximum allowed message size
   * @param {Function} callback A listener for the 'listening' event
   */
</span>  constructor (options, callback) {
    super();

    options = Object.assign({
      maxPayload: 100 * 1024 * 1024,
      perMessageDeflate: true,
      handleProtocols: null,
      clientTracking: true,
      verifyClient: null,
      noServer: false,
      backlog: null, // use default (511 as implemented in net.js)
      server: null,
      host: null,
      path: null,
      port: null
    }, options);

    if (options.port == null && !options.server && !options.noServer) {
      throw new TypeError('missing or invalid options');
    }

    if (options.port != null) {
      this._server = http.createServer((req, res) => {
        const body = http.STATUS_CODES[426];

        res.writeHead(426, {
          'Content-Length': body.length,
          'Content-Type': 'text/plain'
        });
        res.end(body);
      });
      this._server.allowHalfOpen = false;
      this._server.listen(options.port, options.host, options.backlog, callback);
    } else if (options.server) {
      this._server = options.server;
    }

    if (this._server) {
      this._ultron = new Ultron(this._server);
      this._ultron.on('listening', () => this.emit('listening'));
      this._ultron.on('error', (err) => this.emit('error', err));
      this._ultron.on('upgrade', (req, socket, head) => {
        this.handleUpgrade(req, socket, head, (client) => {
          this.emit('connection${req.url}', client);
          this.emit('connection', client);
        });
      });
    }

    if (options.clientTracking) this.clients = new Set();
    this.options = options;
    this.path = options.path;
  }

  /**
   * Close the server.
   *
   * @param {Function} cb Callback
   * @public
   */
  close (cb) {
    //
    // Terminate all associated clients.
    //
    if (this.clients) {
      for (const client of this.clients) client.terminate();
    }

    const server = this._server;

    if (server) {
      this._ultron.destroy();
      this._ultron = this._server = null;

      //
      // Close the http server if it was internally created.
      //
      if (this.options.port != null) return server.close(cb);
    }

    if (cb) cb();
  }

  /**
   * See if a given request should be handled by this server instance.
   *
   * @param {http.IncomingMessage} req Request object to inspect
   * @return {Boolean} 'true' if the request is valid, else 'false'
   * @public
   */
  shouldHandle (req) {
    if (this.options.path && url.parse(req.url).pathname !== this.options.path) {
      return false;
    }

    return true;
  }

  /**
   * Handle a HTTP Upgrade request.
   *
   * @param {http.IncomingMessage} req The request object
   * @param {net.Socket} socket The network socket between the server and client
   * @param {Buffer} head The first packet of the upgraded stream
   * @param {Function} cb Callback
   * @public
   */
  handleUpgrade (req, socket, head, cb) {
    socket.on('error', socketError);

    const version = +req.headers['sec-websocket-version'];

    if (
      req.method !== 'GET' || req.headers.upgrade.toLowerCase() !== 'websocket' ||
      !req.headers['sec-websocket-key'] || ...
```
- example usage
```shell
...

To disable the extension you can set the 'perMessageDeflate' option to 'false'.
On the server:

'''js
const WebSocket = require('ws');

const wss = new WebSocket.Server({
  perMessageDeflate: false,
  port: 8080
});
'''

On the client:
...
```



# <a name="apidoc.module.ws.BufferUtil"></a>[module ws.BufferUtil](#apidoc.module.ws.BufferUtil)

#### <a name="apidoc.element.ws.BufferUtil.concat"></a>[function <span class="apidocSignatureSpan">ws.BufferUtil.</span>concat (list, totalLength)](#apidoc.element.ws.BufferUtil.concat)
- description and source-code
```javascript
(list, totalLength) => {
  const target = Buffer.allocUnsafe(totalLength);
  var offset = 0;

  for (var i = 0; i < list.length; i++) {
    const buf = list[i];
    buf.copy(target, offset);
    offset += buf.length;
  }

  return target;
}
```
- example usage
```shell
...
 * @public
 */
const format = (value) => {
  return Object.keys(value).map((token) => {
    var paramsList = value[token];
    if (!Array.isArray(paramsList)) paramsList = [paramsList];
    return paramsList.map((params) => {
      return [token].concat(Object.keys(params).map((k) => {
        var p = params[k];
        if (!Array.isArray(p)) p = [p];
        return p.map((v) => v === true ? k : '${k}=${v}').join('; ');
      })).join('; ');
    }).join(', ');
  }).join(', ');
};
...
```

#### <a name="apidoc.element.ws.BufferUtil.mask"></a>[function <span class="apidocSignatureSpan">ws.BufferUtil.</span>mask (source, mask, output, offset, length)](#apidoc.element.ws.BufferUtil.mask)
- description and source-code
```javascript
(source, mask, output, offset, length) => {
  for (var i = 0; i < length; i++) {
    output[offset + i] = source[i] ^ mask[i & 3];
  }
}
```
- example usage
```shell
...
  target[1] = payloadLength | 0x80;
  target[offset - 4] = mask[0];
  target[offset - 3] = mask[1];
  target[offset - 2] = mask[2];
  target[offset - 1] = mask[3];

  if (merge) {
    bufferUtil.mask(data, mask, target, offset, data.length);
    return [target];
  }

  bufferUtil.mask(data, mask, data, 0, data.length);
  return [target, data];
}
...
```

#### <a name="apidoc.element.ws.BufferUtil.unmask"></a>[function <span class="apidocSignatureSpan">ws.BufferUtil.</span>unmask (buffer, mask)](#apidoc.element.ws.BufferUtil.unmask)
- description and source-code
```javascript
(buffer, mask) => {
  // Required until https://github.com/nodejs/node/issues/9006 is resolved.
  const length = buffer.length;
  for (var i = 0; i < length; i++) {
    buffer[i] ^= mask[i & 3];
  }
}
```
- example usage
```shell
...
  getData () {
var data = constants.EMPTY_BUFFER;

if (this.payloadLength) {
  if (!this.hasBufferedBytes(this.payloadLength)) return;

  data = this.readBuffer(this.payloadLength);
  if (this.masked) bufferUtil.unmask(data, this.mask);
}

if (this.opcode > 0x07) {
  this.controlMessage(data);
} else if (this.compressed) {
  this.state = INFLATING;
  this.decompress(data);
...
```



# <a name="apidoc.module.ws.Constants"></a>[module ws.Constants](#apidoc.module.ws.Constants)

#### <a name="apidoc.element.ws.Constants.NOOP"></a>[function <span class="apidocSignatureSpan">ws.Constants.</span>NOOP ()](#apidoc.element.ws.Constants.NOOP)
- description and source-code
```javascript
() => {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ws.ErrorCodes"></a>[module ws.ErrorCodes](#apidoc.module.ws.ErrorCodes)

#### <a name="apidoc.element.ws.ErrorCodes.isValidErrorCode"></a>[function <span class="apidocSignatureSpan">ws.ErrorCodes.</span>isValidErrorCode (code)](#apidoc.element.ws.ErrorCodes.isValidErrorCode)
- description and source-code
```javascript
isValidErrorCode = function (code) {
  return (code >= 1000 && code <= 1013 && code !== 1004 && code !== 1005 && code !== 1006) ||
    (code >= 3000 && code <= 4999);
}
```
- example usage
```shell
...
this.loop = false;
this.cleanup(this.cleanupCallback);
      } else if (data.length === 1) {
this.error(new Error('invalid payload length'), 1002);
      } else {
const code = data.readUInt16BE(0, true);

if (!ErrorCodes.isValidErrorCode(code)) {
  this.error(new Error('invalid status code: ${code}'), 1002);
  return;
}

const buf = data.slice(2);

if (!isValidUTF8(buf)) {
...
```



# <a name="apidoc.module.ws.EventTarget"></a>[module ws.EventTarget](#apidoc.module.ws.EventTarget)

#### <a name="apidoc.element.ws.EventTarget.addEventListener"></a>[function <span class="apidocSignatureSpan">ws.EventTarget.</span>addEventListener (method, listener)](#apidoc.element.ws.EventTarget.addEventListener)
- description and source-code
```javascript
addEventListener(method, listener) {
  if (typeof listener !== 'function') return;

  function onMessage (data, flags) {
    listener.call(this, new MessageEvent(data, !!flags.binary, this));
  }

  function onClose (code, message) {
    listener.call(this, new CloseEvent(code, message, this));
  }

  function onError (event) {
    event.type = 'error';
    event.target = this;
    listener.call(this, event);
  }

  function onOpen () {
    listener.call(this, new OpenEvent(this));
  }

  if (method === 'message') {
    onMessage._listener = listener;
    this.on(method, onMessage);
  } else if (method === 'close') {
    onClose._listener = listener;
    this.on(method, onClose);
  } else if (method === 'error') {
    onError._listener = listener;
    this.on(method, onError);
  } else if (method === 'open') {
    onOpen._listener = listener;
    this.on(method, onOpen);
  } else {
    this.on(method, listener);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ws.EventTarget.removeEventListener"></a>[function <span class="apidocSignatureSpan">ws.EventTarget.</span>removeEventListener (method, listener)](#apidoc.element.ws.EventTarget.removeEventListener)
- description and source-code
```javascript
removeEventListener(method, listener) {
  const listeners = this.listeners(method);

  for (var i = 0; i < listeners.length; i++) {
    if (listeners[i] === listener || listeners[i]._listener === listener) {
      this.removeListener(method, listeners[i]);
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ws.Extensions"></a>[module ws.Extensions](#apidoc.module.ws.Extensions)

#### <a name="apidoc.element.ws.Extensions.format"></a>[function <span class="apidocSignatureSpan">ws.Extensions.</span>format (value)](#apidoc.element.ws.Extensions.format)
- description and source-code
```javascript
(value) => {
  return Object.keys(value).map((token) => {
    var paramsList = value[token];
    if (!Array.isArray(paramsList)) paramsList = [paramsList];
    return paramsList.map((params) => {
      return [token].concat(Object.keys(params).map((k) => {
        var p = params[k];
        if (!Array.isArray(p)) p = [p];
        return p.map((v) => v === true ? k : '${k}=${v}').join('; ');
      })).join('; ');
    }).join(', ');
  }).join(', ');
}
```
- example usage
```shell
...

if (props.length) {
  const serverExtensions = props.reduce((obj, key) => {
    obj[key] = [extensions[key].params];
    return obj;
  }, {});

  headers.push('Sec-WebSocket-Extensions: ${Extensions.format(serverExtensions)}');
}

//
// Allow external modification/inspection of handshake headers.
//
this.emit('headers', headers);
...
```

#### <a name="apidoc.element.ws.Extensions.parse"></a>[function <span class="apidocSignatureSpan">ws.Extensions.</span>parse (value)](#apidoc.element.ws.Extensions.parse)
- description and source-code
```javascript
(value) => {
  value = value || '';

  const extensions = {};

  value.split(',').forEach((v) => {
    const params = v.split(';');
    const token = params.shift().trim();
    const paramsList = extensions[token] = extensions[token] || [];
    const parsedParams = {};

    params.forEach((param) => {
      const parts = param.trim().split('=');
      const key = parts[0];
      var value = parts[1];

      if (value === undefined) {
        value = true;
      } else {
        // unquote value
        if (value[0] === '"') {
          value = value.slice(1);
        }
        if (value[value.length - 1] === '"') {
          value = value.slice(0, value.length - 1);
        }
      }
      (parsedParams[key] = parsedParams[key] || []).push(value);
    });

    paramsList.push(parsedParams);
  });

  return extensions;
}
```
- example usage
```shell
...
res.send({ msg: "hello" });
});

const server = http.createServer(app);
const wss = new WebSocket.Server({ server });

wss.on('connection', function connection(ws) {
const location = url.parse(ws.upgradeReq.url, true);
// You might use location.query.access_token to authenticate or share sessions
// or ws.upgradeReq.headers.cookie (see http://stackoverflow.com/a/16395220/151312)

ws.on('message', function incoming(message) {
  console.log('received: %s', message);
});
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
