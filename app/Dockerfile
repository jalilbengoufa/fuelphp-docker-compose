FROM php:5.6-fpm

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
ENV DOCKER true

RUN php -v
RUN apt-get update
RUN apt-get install -y mysql-client vim net-tools telnet curl 
RUN docker-php-ext-install mysql
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo pdo_mysql
RUN bash -c "curl -sS https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer"

RUN mkdir /var/run/php-fpm
COPY php-fpm.d  /usr/local/etc/php-fpm.d
COPY php /usr/local/etc/php

