# Laravel PHP Runtime

![Build](https://github.com/chivincent-rosetta/laravel-runtime/workflows/Build%20Docker%20Images/badge.svg)

This repository is Laravel PHP Runtime docker image builder.

## Usage

### How to build images

```
$ docker build -f php-fpm.dockerfile .
$ docker build -f php-cli.dockerfile .
$ docker build -f php-apache.dockerfile .
```

### How to use images

```
$ docker run --rm -it ghcr.io/chivincent-rosetta/laravel-php:fpm /bin/bash
$ docker run --rm -it ghcr.io/chivincent-rosetta/laravel-php:cli /bin/bash
$ docker run --rm -it ghcr.io/chivincent-rosetta/laravel-php:apache /bin/bash
```

## Q&A

### Why not ARM?

- PHP JIT in PHP 8.0 is not support ARM.
- QEMU + Buildx for `linux/arm64` is slow 5 times than `linux/amd64`.

## License

This repository is under [GPLv3](https://www.gnu.org/licenses/gpl-3.0.html) license.
