FROM php:7.2-fpm

MAINTAINER yf-wu@qq.com


RUN apt-get update && apt-get install -y wget libfreetype6 libfreetype6-dev libmcrypt-dev libmcrypt4 libcurl3-dev \
&& apt install  -y build-essential libprotobuf-dev libboost-dev openssl protobuf-compiler \
&& docker-php-ext-install pdo pdo_mysql

# 安装 swoole
RUN wget https://github.com/swoole/swoole-src/archive/v4.2.2.tar.gz -O swoole.tar.gz \
    && mkdir -p swoole \
    && tar -xf swoole.tar.gz -C swoole --strip-components=1 \
    && rm swoole.tar.gz \
    && cd swoole \
	&& phpize \
	&& ./configure \
	&& make -j$(nproc) \
	&& make install \
    && cd ..  \
	&& rm -r swoole \
    && docker-php-ext-enable swoole

