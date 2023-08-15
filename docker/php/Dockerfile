FROM php:8.2-fpm-alpine

WORKDIR /var/www/html

RUN docker-php-ext-install pdo pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

COPY . .

RUN composer i --no-dev -o

RUN chown -R www-data:www-data /var/www/html
