FROM adminer:4.8.1

EXPOSE 8080

# Switch current user to root to have permission to run commands
USER root

RUN apk update
RUN apk add autoconf gcc g++ make libffi-dev openssl-dev

# MongoDB
RUN pecl install mongodb
RUN echo "extension=mongodb.so" > /usr/local/etc/php/conf.d/docker-php-ext-mongodb.ini

USER adminer
