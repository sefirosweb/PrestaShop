FROM prestashop/prestashop-git:7.2
RUN pecl install xdebug && docker-php-ext-enable xdebug

# To run files with the same group as your primary user
RUN groupmod -g 1000 www-data \
    && usermod -u 1000 -g 1000 www-data

RUN mkdir -p /var/www/.npm
RUN chown -R www-data:www-data /var/www/.npm

# These two directories are docker mounted volumes
RUN chown -R www-data:www-data /var/www/html/vendor
RUN chown -R www-data:www-data /var/www/html/var
