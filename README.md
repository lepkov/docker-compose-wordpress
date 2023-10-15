# docker-compose-wordpress

### Infra for developing a WordPress site with needed php extensions
Contains: PHP 7.4 + Apache2 + MariaDB + phpMyAdmin

## Start infra
'docker-compose up -d'

## Upload a WordPress Website
* Go to 'localhost:8081'
* Login to the phpMyAdmin with root/my_password
* Upload your exported DB
* Upload the website's root dir into the '/app' folder
* Make changes to the wp-config.php with the new DB credentials
* 
