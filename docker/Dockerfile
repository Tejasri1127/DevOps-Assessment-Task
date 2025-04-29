FROM php:8.1-apache

# Install PHP extensions
RUN docker-php-ext-install pdo pdo_mysql mysqli

# Enable Apache mod_rewrite
RUN a2enmod rewrite

# Set working directory
WORKDIR /var/www/html

# Copy Yii2 app files
COPY . /var/www/html/

# Set permissions (for Yii2 runtime)
RUN chown -R www-data:www-data /var/www/html/runtime /var/www/html/web/assets

EXPOSE 80

CMD ["apache2-foreground"]

