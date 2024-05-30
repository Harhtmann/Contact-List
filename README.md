# アプリ名　 Contact-List

## 環境構築

1.リポジトリの作成

1.1. git clone
クローンしたファイル
git@github.com:coachtech-material/laravel-docker-template.git

1.2. docker-compose up -d --build

2.開発環境構築

2.1. docker-compose exec php bash

2.2. composer install

2.3. cp .env.example .env
.env.example ファイルをコピーして env ファイルを作成し、.env ファイル内の 11 行以降を以下のように変更
// 前略

    DB_CONNECTION=mysql

    - DB_HOST=127.0.0.1

    * DB_HOST=mysql
    DB_PORT=3306

    - DB_DATABASE=laravel
    - DB_USERNAME=root
    - DB_PASSWORD=

    * DB_DATABASE=laravel_db
    * DB_USERNAME=laravel_user
    * DB_PASSWORD=laravel_pass

    // 後略

4.php artisan migrate 　未完
5.php artisan db:seed 　未完

## 使用技術(実行環境)

PHP:7.4.9
Laravel:8.83.8
Nginx:1.21.1
MySQL:8.0.26

## ER 図

## URL

開発環境：http//localhost/
phpMyadmin:http//localhost:8080/
