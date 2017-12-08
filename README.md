# Docker PHP / PHP + Apache

This is a PHP docker image built on Alpine Linux (http://www.alpinelinux.org/), a lightweight Linux distro.

## Prerequisites

The following requirements are the environments the image has been tested on.

- Docker version 17.09.0-ce, build afdb6d4
- (Optional) Docker-compose version 1.16.1, build 6d1ac219

## Deployment

Grab the image from the Docker repository.

***PHP 7***

```shell
docker pull johnnyhuy/php:7
```

***PHP 7 + Apache 2.4***

```shell
docker pull johnnyhuy/php:7-apache
```

### Docker Compose

You can use the following configuration to launch the image from docker-compose.

Replace the square brackets with relevant information.

***PHP 7***

```yml
version: "3.2"
services:
  [IMAGE_NAME]:
    image: johnnyhuy/php:7
    volumes:
      - [WEBSITE PATH]:/var/www/live
    ports:
      - 9000:9000
```


***PHP 7 + Apache 2.4***

```yml
version: "3.2"
services:
  [IMAGE_NAME]:
    image: johnnyhuy/php:7-apache
    volumes:
      - [WEBSITE PATH]:/var/www/live
    ports:
      - 80:80
```
