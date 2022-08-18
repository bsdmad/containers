#
# Apache 2.4 + PHP 5.6 for MT
#
FROM php:5.6-apache

# 必要なパッケージの導入
RUN apt-get update && \
      apt-get install -y libdbi-perl libdbd-mysql-perl libhtml-parser-perl \
                         libgd3 libgd-perl exim4 \
                      --no-install-recommends && \
      docker-php-ext-install mysql mysqli && \
    rm -rf /var/lib/apt/lists/*
