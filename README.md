# docker_php7.4

## DocumentRoot is php/html/myapp/public
Please deploy your code in DocumentRoot

but volumes is ./php/html:/var/www/html in docker-compose.yml

Example.

rm -rf myapp

AND 

composer create-project --prefer-dist "laravel/laravel=" myapp

## Web
http://localhost

## phpMyAdmin
http://localhost:8080
