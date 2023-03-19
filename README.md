# Docker-PHP-Dev ![Docker build](https://github.com/J3-Tech/Docker-PHP-Dev/actions/workflows/docker-publish.yml/badge.svg)

Composer-loaded PHP

Install tools:
 - Codesniffer
 - Mess Detector
 - Copy paste detector
 - line of code
 - linter


Usage:

- docker-compose.yml:

```yml
version: '3'

services:
  php:
    image: ghcr.io/j3-tech/docker-php-dev:main
```

- Dockerfile:

```Dockerfile
FROM ghcr.io/j3-tech/docker-php-dev:main

RUN install-php-extensions gd
```