# docker-compose-wordpress

### Infra for developing a WordPress website that includes all needed PHP extensions
Contains: PHP 7.4 + Apache2.4 + MariaDB 10.6 + phpMyAdmin

## Manage infra
`docker-compose up -d`
`docker-compose down`

## Upload a WordPress Website
* Open `localhost:8081` in the browser
* Login to the phpMyAdmin with `root/my_password`
* Upload your exported DB
* Upload the website's root dir into the `/app` folder
* Make changes to the `wp-config.php` with the new DB credentials
* Open `localhost` in the browser to check your website

Apache `access.log` and `error.log` are in the `/app/log` folder
