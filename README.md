# docker-laravel

## Docker 構成

### web container

    nginx: 1.20-alpine

### app container

    PHP: 8.1-fpm
    Composer: 2.0
    Laravel(Breeze, Inertia): 9.X
    Vuejs: 3.x

### db container

    MySql: 8.0

### ngrok container
    ngrokでユーザ登録
    https://dashboard.ngrok.com/signup
    
    ローカルで起動
    $ ngrok http 8080

### mailhog container

    http://localhost:8025/

## 環境構築

    $ docker compose up -d --build
    $ docker compose exec app bash
      /work# composer install
      /work# cp .env.example .env
      /work# php artisan key:generate
      /work# php artisan storage:link
      /work# chmod -R 777 storage bootstrap/cache
      /work# exit

https://localhost
