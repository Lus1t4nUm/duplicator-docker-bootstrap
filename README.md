# Duplicator Docker Bootstrap #
I made this bootstrap for deploying a duplicator backup up and running. Featuring PHP 7, Nginx. You only have to place the backup contents in duplicator/content folder. and Enjoy! 

This bootstrap uses:
[alpine-mariadb](https://github.com/yobasystems/alpine-mariadb) and [alpine-php-wordress](https://github.com/yobasystems/alpine-php-wordpress/releases)
You can check the image in [Dockerhub](https://hub.docker.com/r/yobasystems/alpine-php-wordpress/) and even if you want to install more PHP packages. 

## Building your backup ##

The source code is available here from GitHub:
1. `git clone https://github.com/Lus1t4nUm/duplicator-docker-bootstrap`
2. `cd duplicator-docker-bootstrap`
3. `mkdir duplicator/content`
4. Place your backups files, .zip and installer.php in ./duplicator/content
5. `docker-compose up --build`
6. open http://{SiteDomain}/installer.php in your Browser
7. Install using the native Duplicator installer (as shown in picture):
![picture alt](https://image.ibb.co/dhMKW8/Screen_Shot_2018_07_29_at_21_38_32.png=340 "Database configuration")
    *  Host: {sitedomain} 
    *  User: wordpressuser
    *  Password: wordpresspass
    *  Database: wordpressdb


:exclamation: You have to change the database credentials in docker-compose.yml if you want to deploy in production.


