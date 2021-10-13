FROM php:8.0-fpm

RUN apt-get update
RUN apt-get install -y zlib1g-dev g++ git libicu-dev zip libzip-dev libxml2-dev
RUN apt-get install -y libz-dev libmemcached-dev

# Install extensions
RUN docker-php-ext-install bcmath intl opcache pdo pdo_mysql soap

# Pecl installs
RUN pecl install memcached
RUN pecl install apcu

RUN docker-php-ext-enable memcached apcu

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Symfony cmd tool
RUN curl -sS https://get.symfony.com/cli/installer | bash
RUN mv /root/.symfony/bin/symfony /usr/local/bin/symfony