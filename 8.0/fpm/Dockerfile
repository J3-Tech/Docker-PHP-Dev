FROM php:8.0-fpm

RUN apt-get update \
    && apt-get install -yqq apt-transport-https ca-certificates git unzip wget

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions @composer

COPY .composer /root/.composer
RUN composer global install
