#### Instructions

Clone the repo

```
git clone https://github.com/rewebcan/laravel-docker-quickstart
```

Understanding `docker-compose.yml` and `Dockerfile` will help you quickstart your containerized Laravel application.

##### Starting server

```
docker-compose up -d
```

##### Explanation service by service

There are 3 main service

app, webserver and db

`app` is classic laravel project which can be configured with debugging mode.

`webserver` is nginx service which is configured to run with php-fpm

`db` is a mysql image.

All service has a config folder relatively - mysql, php and nginx

You can remove xdebug arg from docker-compose.yml file to start without xdebug installed

```yaml
app:
    build:
        context: .
        dockerfile: Dockerfile
        args:
            - xdebug=true
```
