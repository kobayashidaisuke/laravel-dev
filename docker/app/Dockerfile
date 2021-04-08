FROM php:8.0-fpm

# install composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer
ENV COMPOSER_ALLOW_SUPERUSER 1

RUN apt-get update \
  && apt-get install -y libonig-dev libzip-dev unzip mariadb-client \
  && docker-php-ext-install pdo_mysql mysqli mbstring zip

WORKDIR /var/www/html
