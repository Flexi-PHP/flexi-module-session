# Session Module

The Session module adapts PHP native sessions to `Flexi\Contracts\Interfaces\SessionStorageInterface` and exposes the `session` service alias.

## Configuration

`Config/services.json` defines the session service and PHP session options, including cookie name, path, domain, secure and HTTP-only flags, and strict mode. Review and override these values for each deployment; use secure cookies over HTTPS and an application-appropriate cookie domain.

The configured adapter uses the `logger` service, so this module requires the Logging module. Install `flexi/flexi-module-session` and activate `Session` after its dependencies. It supports PHP 7.4+, Flexi Core `^3.2`, and `flexi/contracts` `^5.2.1`.

## Tests

Install the development dependencies with `composer install`, then run `vendor/bin/phpunit tests` from the module root.
