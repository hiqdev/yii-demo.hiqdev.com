# yii-demo.hiqdev.com

## Installation for local development

```sh
ln -s core/docker-compose.yml.local docker-compose.yml
ln -s .env.local .env
ln -s public web
composer update
chmod a+w public/assets runtime
docker-compose up -d
```

Web symlink actually not needed.
To be fixed in `yiisoftware/yii2-php:7.2-apache` docker image.

## Installation for production

```sh
ln -s docker-compose.yml.dist docker-compose.yml
ln -s .env.dist .env
composer update
chmod a+w public/assets runtime
docker-compose up -d
```
