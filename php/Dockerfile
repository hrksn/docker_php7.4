FROM php:7.4-apache

RUN docker-php-ext-install pdo_mysql

COPY conf/php.ini /usr/local/etc/php/conf.d/
COPY 000-default.conf /etc/apache2/sites-enabled/

# Composerのインストール
RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer

#npmのインストール
COPY --from=node /usr/local/bin /usr/local/bin
COPY --from=node /usr/local/lib /usr/local/lib

RUN apt-get update \
    && apt-get install -y libicu-dev libzip-dev zlib1g-dev unzip vim \
    && docker-php-ext-install mysqli intl zip

RUN a2enmod rewrite