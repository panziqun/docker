FROM php:7.2-fpm

COPY ./amqp-1.9.4.tgz /tmp/amqp-1.9.4.tgz

RUN apt-get update \
    && apt-get install -y librabbitmq-dev \
    && pecl install /tmp/amqp-1.9.4.tgz
# RUN docker-php-ext-install mbstring