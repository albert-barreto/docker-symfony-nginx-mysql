# Symfony Docker-Development-Stack
This is a lightweight stack based on Alpine Linux for running Symfony 5 into Docker containers using docker compose. 

### Prerequisites
* [Docker](https://www.docker.com/)

### Container
 - [php-fpm](https://hub.docker.com/_/php) 8.0
    - [composer](https://getcomposer.org/) 
    - [yarn](https://yarnpkg.com/lang/en/) and [node.js](https://nodejs.org/en/) (if you will use [Encore](https://symfony.com/doc/current/frontend/encore/installation.html) for managing JS and CSS)
- [nginx](https://hub.docker.com/_/nginx) 1.21.+
- [mysql](https://hub.docker.com/_/mysql/) 5.7.+

### Installing

run docker and connect to container:
```
 docker compose up --build
```
```
 docker compose exec php sh
```

install the latest version of [Symfony](http://symfony.com/doc/current/setup.html) via composer:
```
# traditional web application: 
composer create-project symfony/website-skeleton .
```
or 
```
# microservice, console application or API:
composer create-project symfony/skeleton .
```

modify your DATABASE_URL config in .env 
```
DATABASE_URL=mysql://root:root@mysql:3306/symfony?serverVersion=5.7
```

### Ready up
call [localhost](http://localhost/) in your browser
