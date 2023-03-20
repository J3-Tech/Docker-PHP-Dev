FROM php:8.2-fpm

RUN apt-get update \
    && apt-get install -y apt-transport-https ca-certificates git unzip wget

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions @composer

COPY .composer /root/.composer
RUN composer global install
