# Laravel Psalm Helper

A zero-config installer for Psalm (a static analysis tool that’s designed to improve large PHP codebases by identifying both obvious and hard-to-spot bugs)

[![Required: PHP7.2](https://img.shields.io/packagist/php-v/socheatsok78/laravel-psalm-helper)](https://packagist.org/packages/socheatsok78/laravel-psalm-helper) [![packagis](https://img.shields.io/packagist/v/socheatsok78/laravel-psalm-helper)](https://packagist.org/packages/socheatsok78/laravel-psalm-helper) [![packagis-download](https://img.shields.io/packagist/dm/socheatsok78/laravel-psalm-helper)](https://packagist.org/packages/socheatsok78/laravel-psalm-helper) [![License](https://img.shields.io/github/license/socheatsok78/laravel-psalm-helper)](./LICENSE)

## Installaion
```bash
composer require --dev socheatsok78/laravel-psalm-helper
```

Add the following script to `composer.json`:
```json
"scripts": {
    "psalm": [
        "vendor/bin/psalm --show-info=false"
    ],
    "psalm:info": [
        "vendor/bin/psalm --show-info=true"
    ],
    "psalm:dry-run": [
        "vendor/bin/psalm --alter --issues=InvalidReturnType,InvalidNullableReturnType --dry-run"
    ],
    "psalm:alter": [
        "vendor/bin/psalm --alter --issues=InvalidReturnType,InvalidNullableReturnType"
    ]
}
```
Then later you can just run `composer run psalm`

### Usage

Add a `psalm.xml` config:

```bash
./vendor/bin/psalm --init [source_directory=src] [config_level=3]
```

where `config_level` represents how strict you want Psalm to be. `1` is the strictest, `8` is the most lenient.

Example:
```console
$ ./vendor/bin/psalm --init
Config file created successfully. Please re-run psalm.

$ ./vendor/bin/psalm-plugin enable psalm/plugin-laravel
[OK] Plugin enabled
```

Then run Psalm:

```bash
./vendor/bin/psalm
```

See more at [Psalm Documentation](https://psalm.dev/docs/)

## What's inside?

This package will only install the following dependencies:
- [vimeo/psalm](https://github.com/vimeo/psalm)
- [psalm/laravel-psalm-plugin](https://github.com/psalm/laravel-psalm-plugin)

## :memo: License

Licensed under the [MIT License](./LICENSE).
