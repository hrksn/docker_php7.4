# docker_php7.4_framework

## DocumentRoot is php/html/myapp/public
Please deploy your code in DocumentRoot

docker-compose up -d

TEST: http://localhost

TEST OK -> rm -rf php/html/myapp

AND 

cd php/html

composer create-project --prefer-dist "laravel/laravel=" myapp

## Web
http://localhost

## phpMyAdmin
http://localhost:8080
