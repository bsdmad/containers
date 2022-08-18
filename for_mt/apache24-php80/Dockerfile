#
# Apache 2.4 + PHP 8.0 for MT
#
FROM php:8.0-apache

# 必要なパッケージの導入
RUN apt-get update && \
      apt-get install -y libdbi-perl libdbd-mysql-perl libhtml-parser-perl \
                         libgd3 libgd-perl exim4 \
                      --no-install-recommends && \
      docker-php-ext-install mysqli && \
    rm -rf /var/lib/apt/lists/*
