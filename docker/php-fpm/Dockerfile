FROM phpdockerio/php:7.4-fpm
WORKDIR "/crud"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php7.4-pgsql php7.4-gd php7.4-redis php7.4-curl php7.4-zip\
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/* \

RUN sudo chmod -R 777 /var/www/html/crud/storage

