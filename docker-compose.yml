version: '3'
services:
  php:
    image: php:8.2-fpm
    container_name: php
    volumes:
      - ./project:/var/www/html

  nginx:
    image: nginx:latest
    container_name: nginx
    ports:
      - "80:80"
    volumes:
      - ./project:/var/www/html
      - ./nginx.conf:/etc/nginx/conf.d/default.conf
    depends_on:
      - php
