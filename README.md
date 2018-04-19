# Docker Template for Laravel applications


## Clone this repo

```
$ git clone https://github.com/7nohe/laravel-docker-template.git
```

## Create docker images and containers

```
$ docker-compose build
# or
$ docker-compose build --build-arg INSTALL_XDEBUG=true
$ docker-compose up -d
```

## Create a laravel application

```
$ docker-compose exec php laravel new
$ cp server/.env.example .env
$ docker-compose exec php php artisan key:generate
$ docker-compose exec php php artisan migrate
```


Open http://localhost:8080 in your browser.

## Xdebug setup

/server/docker/php/php.ini

```
zend_extension=xdebug.so
xdebug.remote_enable = 1
xdebug.remote_autostart = 1
xdebug.remote_port = 9001
xdebug.idekey = DOCKER
xdebug.remote_host = YOUR_HOST
```


