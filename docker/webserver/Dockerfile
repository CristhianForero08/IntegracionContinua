FROM webdevops/php-apache-dev:7.3@sha256:5945a05eb7774e57d8519f8fca908af876e0abb82274025fb3baaaa9dfc7babc

RUN apt-get update -y && \
    apt-get install git -y && \
    apt install nodejs -y && \
    apt install npm -y

WORKDIR /home/application/.ssh
COPY docker/gitlab/* .

COPY docker/webserver/openssl/openssl.cnf /etc/ssl/

RUN chown -R application:application ../ && \
    chmod 600 *

