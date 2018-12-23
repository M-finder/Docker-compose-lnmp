FROM php:7.2-fpm

MAINTAINER yf-wu@qq.com


RUN apt-get update && apt-get install -y libfreetype6 libfreetype6-dev libmcrypt-dev libmcrypt4 libcurl3-dev && apt install  -y build-essential libprotobuf-dev libboost-dev openssl protobuf-compiler && docker-php-ext-install pdo pdo_mysql

