# Additional Setup for Nextcloud

In order to load imagick with the current docker image run the following set of command:

- docker exec -it nextcloud sh
- apk add --update --no-cache autoconf g++ imagemagick imagemagick-dev libtool make pcre-dev \
    && pecl install imagick \
    && docker-php-ext-enable imagick \
    && apk del autoconf g++ libtool make pcre-dev
- Press enter when prompted

Ensure that imagick is install using the following command:

- php -i | grep ImageMagick

References:

- https://ghost.rivario.com/docker-php-7-2-fpm-alpine-imagick/
