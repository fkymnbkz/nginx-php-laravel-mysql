# README

| | |
|:--|:--|
| nginx | 1.17 |
| MySql | 5.7.12 |
| PHP | 7.4 |
| Laravel | 6.8 |

## Directory

``` bash
.
├── data        # MySqlのデータディレクトリ
├── dockerfiles # Dockerの設定ファイル群
│   ├── mysql
│   ├── nginx
│   └── php
├── logs        # ログ出力ディレクトリ
├── src         # Laravelインストール先
├── docker-compose.yml
└── README
```

## Initialize

``` bash
docker-compose build
docker-compose up -d
docker-compose exec php ash
/var/www $ composer install
/ver/www $ cp .env.example .env
/var/www $ php artisan key:generate
```

## Mysql

| | |
|:--|:--|
| database | develop |
| user | docker |
| password | docker |
