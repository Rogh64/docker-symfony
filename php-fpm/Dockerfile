FROM alpine:3.12

MAINTAINER Yann Carpentier <yann.carpentier@protonmail.com>

RUN apk add --update \
    php7-fpm \
	php-fpm \
    php7-apcu \
    php7-ctype \
    php7-curl \
    php7-dom \
    php7-gd \
    php7-iconv \
    php7-imagick \
    php7-json \
    php7-intl \
    php7-mcrypt \
    php7-opcache \
    php7-openssl \
	php7-sqlite3 \
    php7-pdo \
    php7-pdo_mysql \
    php7-mysqli \
    php7-xml \
    php7-zlib

RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD symfony.ini /etc/php7/fpm/conf.d/
ADD symfony.ini /etc/php7/cli/conf.d/

ADD symfony.pool.conf /etc/php7/fpm.d/

CMD ["php-fpm7", "-F"]

EXPOSE 9000
