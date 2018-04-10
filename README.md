# Docker Template for Laravel applications


## Clone this repo

```
$ git clone https://github.com/7nohe/laravel-docker-template.git
```

## Create docker images and containers

```
$ docker-compose build
$ docker-compose up -d
```

## Create a laravel application

```
$ docker-compose exec php laravel new
$ cp .env.example src/.env
$ docker-compose exec php php artisan key:generate
$ docker-compose exec php php artisan migrate
```


Open http://localhost:8080 in your browser.


