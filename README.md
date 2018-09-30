# turboServer
High Performance nodeJS HTTP server based on turbo-http

## Request

The first parameter of the handler function is  `Request`:

-   `query`  - the parsed querystring
-   `body`  - the body (?)
-   `params`  - the params matching the URL
-   `headers`  - the headers
-   `id`  - the request id
-   `supports`  - the clients supported web technologies (brotli, webp, ...)
-  `url` the requested url
## Response

The second parameter of the handler function is  `Response`: 
-   `options`  - the options set for the route merged with server options
-   `send`  - sends the body to the client. It accepts Buffers, Strings and Objects/Arrays.
## Options
Options can be set per app and request
with the `setOptions` method. It has 1 Argument that is an Object that can contain the following keys with boolen values except explictly specified:

-   `nocache`  - Cache-Control, Expires, Pragma headers
-   `xdeny` - X-Frame-Options DENY
-   `xsameorigin` - X-Frame-Options SAMEORIGIN
-  `xxss` - X-XSS-Protection 1; mode=block
-  `xcontent` - X-Content-Type-Options nosniff
-  `xdownload` - X-Download-Options noopen
-  `cors` - <String> Access-Control-Allow-Origin
-  `corsmethods` - <String> Access-Control-Allow-Methods          
-  `hsts` - Strict-Transport-Security max-age=31536000
-  `xdns` - X-DNS-Prefetch-Control true-> on, false->off
-  `hideserver` - hides the Server header
-  `brotli` - enable brotli compression
-  `gzip` - enable gzip compression
-  `etag` - X-Frame-Options SAMEORIGIN
