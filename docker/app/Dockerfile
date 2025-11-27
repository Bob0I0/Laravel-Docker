FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    zip unzip git curl \
    && docker-php-ext-install pdo pdo_mysql

COPY php.ini /usr/local/etc/php/

WORKDIR /var/www/html

COPY --from=composer:2 /usr/bin/composer /usr/bin/composer
