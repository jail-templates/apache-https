# Apache 2.4 (http + https)
Bastille template to install and configure the Apache HTTP server with some sane defaults.

* httpd listens on ports 80 (HTTP) and 443 (HTTPS).
* `DocumentRoot` is `/usr/local/www`.
* Some sane defaults:
  * No directory listings by default (`-Indexes`)
  * No following of symlinks by default (`-FollowSymlinks`)
  * No server side includes by default (`-Includes`)
  * Limit methods to GET, POST and HEAD (`LimitExcept`)
  * Disabled TRACE method by default (`TraceEnable off`)
  * Reduced public server information (`ServerTokens Prod`)
  * Reduced `Timeout` of 30 seconds (`Timeout 30`)

## Bootstrap
```
bastille bootstrap https://github.com/jail-templates/apache-https
```

## Apply template
```
bastille template $JAIL jail-templates/apache
```
