FROM drupal:7-fpm

# Download latest stable release using the code below or browse to github.com/drush-ops/drush/releases.
RUN php -r "readfile('http://files.drush.org/drush.phar');" > /tmp/drush

# Test your install.
RUN php /tmp/drush core-status

# Make `drush` executable as a command from anywhere. Destination can be anywhere on $PATH.
RUN chmod +x /tmp/drush
RUN sudo mv /tmp/drush /usr/local/bin
