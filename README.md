# docker-laravel

## Docker 構成

### web container

    nginx: 1.20-alpine

### app container

    PHP: 8.0-fpm-buster
    Composer: 2.0
    Laravel: 8.X

### db container

    MySql: 8.0

## 環境構築

    $ docker compose up -d --build
    $ docker compose exec app bash
      /work# composer install
      /work# composer require laravel/breeze:^1 --dev
      /work# php artisan breeze:install vue
      /work# cp .env.example .env
      /work# php artisan key:generate
      /work# php artisan storage:link
      /work# chmod -R 777 storage bootstrap/cache
      /work# exit

http://127.0.0.1:8080/
