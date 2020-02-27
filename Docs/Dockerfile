# PRAVALER – Exemplo de Dockerfile
FROM ubuntu:18.04

RUN apt-get update && apt-get install -y nginx

RUN apt-get install -y curl php php7.2-bcmath php7.2-bz2 php7.2-mbstring php7.2-pgsql php7.2-zip php7.2-fpm

ADD www.conf /etc/php/7.2/fpm/pool.d/www.conf
ADD entrypoint.sh /usr/local/entrypoint.sh
ADD example_php.conf /etc/nginx/sites-enabled/example_php.conf

ENTRYPOINT ["/bin/sh", "/usr/local/entrypoint.sh"]
