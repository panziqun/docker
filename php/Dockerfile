FROM php:7.2-fpm

COPY ./amqp-1.9.4.tgz /tmp/amqp-1.9.4.tgz

RUN apt-get update \
    && apt-get install -y cron \
    && service cron start \
    && ln -s /usr/local/bin/php /bin/php \
    && apt-get install -y vim \
    && apt-get install -y librabbitmq-dev \
    && pecl install /tmp/amqp-1.9.4.tgz \
    && apt-get install -y supervisor 
# RUN docker-php-ext-install mbstring