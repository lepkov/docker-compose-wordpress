# docker-compose-wordpress-LAMP
LAMP = Linux, Apache, MariaDB, PHP
### Simple Infra/Hosting for developing and troubleshooting a WordPress website that includes all needed PHP extensions 
Contains: 
* PHP 7.4-FPM Container
* Apache 2.4 Container
* MariaDB 10.6 Container
* phpMyAdmin Container

![image](https://github.com/lepkov/docker-compose-wordpress-LAMP/assets/23506790/19e287b6-220e-46a7-beec-51bfbc8a49b5)

## Manage infra
`docker-compose up -d`

`docker-compose down`

## Upload a WordPress Website
* Open `localhost:8081` in the browser
* Login to the phpMyAdmin with `root/my_password`
* Upload your exported DB
* Upload the website's root dir into the `/app` folder
* Make changes to the `wp-config.php` with the new DB credentials and add:
```
define( 'WP_HOME', 'http://localhost' ); 
define( 'WP_SITEURL', 'http://localhost' );
define( 'FS_METHOD', 'direct' );
```
* Make changes in `.htaccess` in paths if they exist
* Open `localhost` in the browser to check your website
## Logs
Apache `apache-access.log` and `apache-error.log` are in the `/app/logs` folder.

MariaDB `mariadb-slow.log` is in the `/app/logs` folder.

PHP-FPM `php-fpm-error.log` is in the `/app/logs` folder.

FYI: No php flags in `.htaccess`, since it is php-fpm, they should be in /etc/php/8.0/fpm/pool.d/example.com.conf - TODO paste the actual path.
