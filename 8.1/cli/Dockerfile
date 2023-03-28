FROM php:8.1-cli

RUN apt-get update \
    && apt-get install -yqq apt-transport-https ca-certificates git unzip wget

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions xdebug @composer

COPY .composer /root/.composer
RUN composer global install
ENV PATH="$PATH:/root/.composer/vendor/bin"
