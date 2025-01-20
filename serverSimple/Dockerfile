FROM php:8.2-fpm

RUN docker-php-ext-install sockets

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /app
COPY . /app

RUN composer install

CMD ["php", "server.php", "config.yaml"]