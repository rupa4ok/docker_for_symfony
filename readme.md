# docker-php-nginx-postgres-composer
Docker Compose configuration to run PHP 7.3 with Nginx, PHP-FPM + PHP-FPM-CLI, PostgreSQL 10.1 and Composer.

## Optionally install 

1) Redis for cache
2) Redis queue server 
3) ELK - elasticsearch - kibana - logstash
4) Centrifugo
5) Rabbitmq
6) Mysql 5.6 or 8.0
7) Node.js 12.7

## Install prerequisites

For now the project has been tested on Linux only but should run fine on Docker for Windows and Docker for Mac.

You will need:

* [Docker CE](https://docs.docker.com/engine/installation/)
* [Docker Compose](https://docs.docker.com/compose/install)

## How to use it

### Starting Docker Compose

Checkout the repository or download the sources.

Simply run `docker-compose up` and you are done.

Nginx will be available on `localhost:8080, localhost:80` and PostgreSQL on `localhost:54321, localhost:5432`.

#### To check the status of containers

run `docker-compose ps`

#### Container logs

run `docker-compose logs <container-name>`

### Using Composer

`docker-compose run --rm manager-php-cli composer`

### Symfony Console

`docker-compose run --rm manager-php-cli php bin/console`
