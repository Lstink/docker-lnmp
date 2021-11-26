FROM php:7.2-fpm-buster
RUN apt-get update && apt-get install -y \
          libwebp-dev \
          libjpeg-dev \
          libpng-dev \
          libfreetype6-dev \
    && docker-php-source extract \
    && cd /usr/src/php/ext/gd \
    && docker-php-ext-configure gd --with-webp-dir=/usr/include/webp --with-jpeg-dir=/usr/include --with-png-dir=/usr/include --with-freetype-dir=/usr/include/freetype2 \
    && docker-php-ext-install gd \
    && docker-php-ext-install bcmath