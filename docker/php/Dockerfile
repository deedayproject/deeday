FROM php:7.2-fpm

RUN apt-get update && \
    apt-get install -y \
        git \
        unzip \
        libpq-dev

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer --version
RUN mkdir /var/www/.composer && chown -R www-data /var/www/.composer

RUN rm /etc/localtime
RUN ln -s /usr/share/zoneinfo/Europe/Paris /etc/localtime
RUN "date"

RUN docker-php-ext-install pdo pdo_pgsql

# ARG GITHUB_TOKEN
# RUN composer config --global --auth github-oauth.github.com ${GITHUB_TOKEN}

RUN echo 'alias sf4="php bin/console"' >> ~/.bashrc

RUN usermod -u 1000 www-data

WORKDIR /var/www/symfony