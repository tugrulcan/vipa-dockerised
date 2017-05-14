FROM phpdockerio/php7-fpm:latest
# The following extensions are already included on the base image: APC, cURL, JSON, MCrypt (libsodium on 7.1), OPCache, Readline, XML and Zip.
# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php7.0-memcached php7.0-pgsql php7.0-sqlite3 php-gd php7.0-gd php7.0-bcmath php7.0-imap php7.0-intl php7.0-mbstring php7.0-xdebug php7.0-xmlrpc php-apcu \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*


WORKDIR "/application"