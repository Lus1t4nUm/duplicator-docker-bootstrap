# Duplicator Docker Bootstrap #
We made this bootstrap for deploying a duplicator backup up and running. Featuring PHP 7, Nginx. You only have to place the backup contents in duplicator/content folder. and Enjoy! 

This bootstrap uses:
[alpine-mariadb](https://github.com/yobasystems/alpine-mariadb) and [alpine-php-wordress](https://github.com/yobasystems/alpine-php-wordpress/releases)
You can check the image in [Dockerhub](https://hub.docker.com/r/yobasystems/alpine-php-wordpress/) and even if you want to install more PHP packages. 

## Building your backup ##

Start by cloning this repo:

1. `git clone https://github.com/rsousacode/duplicator-docker-bootstrap`
2. `cd duplicator-docker-bootstrap`
3. Place your backups files, .zip and installer.php in ./duplicator/content
4. `docker-compose up --build`
5. open http://{SiteDomain}/installer.php in your Browser
6. Install using the native Duplicator installer:
    *  Host: {sitedomain} 
    *  User: wordpressuser
    *  Password: wordpresspass
    *  Database: wordpressdb


:exclamation: You have to change the database credentials in docker-compose.yml if you want to deploy in production.


