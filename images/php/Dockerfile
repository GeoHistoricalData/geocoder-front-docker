FROM php:7.2.3-fpm-stretch

RUN apt-get update && \
    apt-get install -y libpq-dev libxml2-dev

RUN docker-php-ext-install pgsql && \
    docker-php-ext-install xml
