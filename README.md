# PHP OAuth 2.0 Server for Laravel

A wrapper package for the standards compliant OAuth 2.0 authorization server and resource server written in PHP by the [League of Extraordinary Packages](http://www.thephpleague.com)

## Package Installation

### With Laravel Package Installer

The easiest way to install this package is via [Laravel Package Installer](https://github.com/rtablada/package-installer), this will set all the service providers and aliases for you. Run this artisan command to install the package:

```
php artisan package:install lucadegasperi/oauth2-server-laravel
```

### Manual Install

alternatively, you can manually install the package via composer. add the following line to your composer.json file:

```javascript
"lucadegasperi/oauth2-server-laravel": "dev-master"
```

Add this line of code to the ```providers``` array located in your ```app/config/app.php``` file:
```php
'LucaDegasperi\OAuth2Server\OAuth2ServerServiceProvider',
```

And this lines to the ```facades``` array:
```php
'AuthorizationServer' => 'LucaDegasperi\OAuth2Server\Facades\AuthorizationServerFacade',
'ResourceServer' => 'LucaDegasperi\OAuth2Server\Facades\ResourceServerFacade',
```

### Configuration

In order to use the OAuth2 server publish its configuration first

```
php artisan config:publish lucadegasperi/oauth2-server-laravel
```

Afterwards edit the file ```app/config/packages/lucadegasperi/oauth2-server-laravel/oauth2.php``` to suit your needs.

### Migrations

This package comes with all the migrations you might need to run an oauth2 server. Run:

```
php artisan migrate --package="lucadegasperi/oauth2-server-laravel"
```


## Support

Bugs and feature request are tracked on [GitHub](https://github.com/lucadegasperi/oauth2-server-laravel/issues)

## License

This package is released under the MIT License.

## Credits

The code on which this package is [based](https://github.com/php-loep/oauth2-server/), is principally developed and maintained by [Alex Bilbie](https://twitter.com/alexbilbie).
