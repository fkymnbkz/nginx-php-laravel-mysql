# README

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
/var/www $ compose install
/var/www $ php artisan key:generate
```

`.gitignore`にsrcディレクトリが指定されているので削除すること。

## Mysql

| | |
|:--|:--|
| database | develop |
| user | docker |
| password | docker |
