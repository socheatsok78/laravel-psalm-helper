# Laravel Psalm Helper

A zero-config installer for Psalm (a static analysis tool that’s designed to improve large PHP codebases by identifying both obvious and hard-to-spot bugs)

## Installaion
```bash
composer require --dev socheatsok78/laravel-psalm-helper
```

### Usage

Add a `psalm.xml` config:

```bash
./vendor/bin/psalm --init [source_directory=src] [config_level=3]
```

where `config_level` represents how strict you want Psalm to be. `1` is the strictest, `8` is the most lenient.

Example:
```console
$ ./vendor/bin/psalm --init src 3
Config file created successfully. Please re-run psalm.
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
