# Duplicator Docker Bootstrap #
I made this bootstrap for deploying a duplicator backup up and running. Featuring PHP 7, Nginx. You only have to place the backup contents in duplicator/content folder. and Enjoy! 

This bootstrap uses:
[alpine-mariadb](https://github.com/yobasystems/alpine-mariadb) and [alpine-php-wordress](https://github.com/yobasystems/alpine-php-wordpress/releases)
You can check the image in [Dockerhub](https://hub.docker.com/r/yobasystems/alpine-php-wordpress/) and even if you want to install more PHP packages. 

## Building your backup ##

The source code is available here from GitHub:
1. `git clone https://github.com/Lus1t4nUm/duplicator-bootstrap`
2. Place your zip and installer.php in duplicator/content
3. `cd duplicator-docker-bootstrap` 
4. `docker-compose up -d`
5. open http://{SiteDomain}/installer.php in your Browser
6. Install using host: {SiteDomain}; User: wordpressuser Pass: wordpresspass; Db: wordpressdb
~~~
You have to change the database credentials in docker-compose.yml if you want to deploy in production.
~~~

