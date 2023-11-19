# PHP 7.4

FROM php:7.4.33-apache

RUN docker-php-ext-install mysqli

RUN apt-get update && apt-get install -y libpng-dev
RUN apt-get install -y \
    libwebp-dev \
    libjpeg62-turbo-dev \
    libpng-dev libxpm-dev \
    libfreetype6-dev \
    libzip-dev

RUN docker-php-ext-configure gd \
    --with-webp \
    --with-jpeg \
    --with-xpm \
    --with-freetype

RUN docker-php-ext-install gd

RUN apt-get install -y \
    libxml2-dev

RUN docker-php-ext-install simplexml zip