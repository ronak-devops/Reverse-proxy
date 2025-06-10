# web/Dockerfile
FROM php:8.2-fpm

RUN apt update && apt install -y nginx

COPY default.conf /etc/nginx/conf.d/default.conf
COPY index.html /var/www/html/
COPY index.php /var/www/html/

CMD ["sh", "-c", "php-fpm -D && nginx -g 'daemon off;'"]
