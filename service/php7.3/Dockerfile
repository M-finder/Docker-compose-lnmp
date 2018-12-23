FROM php:7.3-fpm

RUN apt-get update && apt-get install -y libfreetype6 libfreetype6-dev libmcrypt-dev libmcrypt4 libcurl3-dev && apt install build-essential libprotobuf-dev libboost-dev openssl protobuf-compiler && docker-php-ext-install pdo pdo_mysql

