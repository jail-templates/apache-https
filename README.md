# Apache 2.4 (HTTP/HTTPS)
Bastille template to install and configure the Apache HTTP Server with some sane defaults.

* httpd listens on ports 80 (HTTP) and 443 (HTTPS).
* `DocumentRoot` is `/usr/local/www`.
* Some sane defaults:
  * No directory listings by default (`-Indexes`).
  * No following of symlinks by default (`-FollowSymlinks`).
  * No server side includes by default (`-Includes`).
  * Limit methods to GET, POST and HEAD (`LimitExcept`).
  * Disabled TRACE method by default (`TraceEnable off`).
  * Reduced public server information (`ServerTokens Prod`).
  * Reduced timeout of 30 seconds (`Timeout`).
* Support for php-fpm:
  * Multi-Processing Module: `mpm_event_module` (switch to `mpm_prefork_module` for `mod_php`).
  * `proxy_module` and `proxy_fcgi` enabled by default (disable when no need for php).
* Shows "It Works!" in a browser if everything is setup correctly.

## Bootstrap
```
bastille bootstrap https://github.com/jail-templates/apache-https
```

## Apply template
```
bastille template $JAIL jail-templates/apache-https
```

## Support
Templates will be maintained until their respective software version is end-of-life. Repositories will then be archived and removed from any meta-templates.

If you have a question, suggestion or find a bug, please let us know via an Issues in the relevant repository or send us an email.

## License
All templates are distributed under the 3-Clause BSD NON-AI License. See `LICENSE` in every template repository for more information.
