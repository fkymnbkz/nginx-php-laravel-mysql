FROM php:7.4.1-fpm-alpine3.11

COPY php.ini /usr/local/etc/php/

RUN apk update && apk add --no-cache \
  freetype-dev libjpeg-turbo-dev libpng-dev libmcrypt-dev libzip-dev oniguruma-dev \
  git vim unzip tzdata libltdl

# RUN docker-php-ext-configure zip --with-libzip=/usr/include

RUN docker-php-ext-install zip mbstring gd iconv \
  && cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
  && apk del tzdata \
  && rm -rf /var/cache/apk/*

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
  chmod +x /usr/local/bin/composer

RUN docker-php-ext-install pdo_mysql bcmath

WORKDIR /var/www
