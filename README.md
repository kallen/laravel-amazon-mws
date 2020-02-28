# Laravel Amazon MWS

Simple Amazon MWS API Package for Laravel

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Latest Version on Packagist](https://img.shields.io/packagist/v/looxis/laravel-amazon-mws.svg?style=flat-square)](https://packagist.org/packages/looxis/laravel-amazon-mws)
![Travis (.org)](https://img.shields.io/travis/looxis/laravel-amazon-mws)
[![StyleCI](https://styleci.io/repos/242777921/shield?branch=master)](https://styleci.io/repos/242777921)
![Scrutinizer build (GitHub/Bitbucket)](https://img.shields.io/scrutinizer/build/g/looxis/laravel-amazon-mws/master)

## Installation

Require the package using composer:

```bash
composer require looxis/laravel-amazon-mws
```

The package will automatically register itself.

Add your Environment Variables for MWS to your .env File. The variable names are listed in the amazon-mws.php config file.

You can optionally publish the configuration with:

php artisan vendor:publish --provider="Looxis\LaravelAmazonMWS\AmazonMWSServiceProvider" --tag="config"
This is the content of the published config file:

```php
<?php

return [
    'access_key_id' => env('MWS_ACCESS_KEY_ID'),
    'secret_key' => env('MWS_SECRET_KEY'),
    'seller_id' => env('MWS_SELLER_ID'),
    'default_market_place' => env('MWS_DEFAULT_MARKET_PLACE', 'DE'),
];
```

## Usage

Using the AmazonMWS you can fetch orders via the orders service class:

```php
$orderResponse = AmazonMWS::orders()->get("1234-1234-1234"); //get amazon order by id
```

## Testing

``` bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Security

If you discover any security related issues, please email dev@looxis.com instead of using the issue tracker.

## Credits

- [Christian Stefener](https://github.com/ChrisSFR)
- [Jannik Malken](https://github.com/mannikj)
- [All Contributors](../../contributors)

## License
[MIT](./LICENSE.md)