FROM alpine:latest

RUN apk add --update \
    php7-fpm \
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
    php7-fileinfo\
    php7-mbstring \
    php7-opcache \
    php7-openssl \
    php7-pdo \
    php7-pdo_mysql \
    php7-mysqli \
    php7-xml \
    php7-zlib \
    php7-phar \
    php7-tokenizer \
    php7-session \
    php7-simplexml \
    php7-xdebug \
    php7-zip \
    make \
    curl \
    ssmtp

RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD php.ini /etc/php7/conf.d/
ADD php.ini /etc/php7/cli/conf.d/
ADD wp.pool.conf /etc/php7/php-fpm.d/
ADD ssmtp.conf /etc/ssmtp/ssmtp.conf

CMD ["php-fpm7", "-F"]

EXPOSE 9001
