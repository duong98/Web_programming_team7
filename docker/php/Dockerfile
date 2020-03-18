FROM php:7.3

WORKDIR /var/www

# Install dependencies
RUN apt-get update

# Install extensions
RUN docker-php-ext-install mbstring bcmath

# XDEBUG
RUN pecl install xdebug
RUN docker-php-ext-enable xdebug
# This needs in order to run xdebug from PhpStorm
ENV PHP_IDE_CONFIG 'serverName=DockerApp'

ADD php.ini /usr/local/etc/php
