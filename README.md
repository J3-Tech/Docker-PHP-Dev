# Docker-PHP-Dev
[![Docker](https://github.com/J3-Tech/Docker-PHP-Dev/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/J3-Tech/Docker-PHP-Dev/actions/workflows/docker-publish.yml)

Composer-loaded PHP

Install tools:
 - Codesniffer
 - Mess Detector
 - Copy paste detector
 - LOC
 - Lint
 - PHP Unit


## Usage:

- docker-compose.yml:

```yml
version: '3'

services:
  php:
    image: ghcr.io/j3-tech/docker-php-dev:main-8.2-cli
    # image: ghcr.io/j3-tech/docker-php-dev:main-8.1-cli
    # image: ghcr.io/j3-tech/docker-php-dev:main-8.0-cli
```

- Dockerfile:

```Dockerfile
FROM ghcr.io/j3-tech/docker-php-dev:main-8.2-cli
# FROM ghcr.io/j3-tech/docker-php-dev:main-8.1-cli
# FROM ghcr.io/j3-tech/docker-php-dev:main-8.0-cli

RUN install-php-extensions gd
```

## Multi platform support

Image supports `amd64`, `arm64`, `i386`, `ppc64le`, and `s390x`
