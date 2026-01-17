#ОПРЕДЕЛЕНИЕ ОБРАЗА ПРОГРАММЫ
FROM nginx:1.29
##RUN rm /etc/nginx/nginx.conf
#СОПОСТАВЛЕНИЕ ПУТЕЙ ФАЙЛОВ РАБОЧЕГО КАТАЛОГА С / ДОКЕР КАТАЛОГАМИ
COPY ./nginx.conf /etc/nginx/nginx.conf
##RUN rm /etc/nginx/conf.d/default.conf
#COPY ./sites-available/nginx_main1.conf /etc/nginx/conf.d/nginx_main_http.conf 
COPY ./sites-available/nginx_main_httpS.conf /etc/nginx/conf.d/nginx_main_httpS.conf
##COPY ./src /З

#COPY ./snippets/main_snakeoil.conf /var/www/html/php_project09082023/config/nginx/snippets/main_snakeoil.conf
#
#COPY ./sites-available/nginx_main_httpS.conf /etc/nginx/conf/fastcgi.conf
COPY ./snippets/fastcgi-php.conf /snippets/fastcgi-php.conf
COPY ./fastcgi_params/fastcgi_params.conf /fastcgi.conf

#МОНТИРОВАНИЕ ТОМА С ПРИВЯЗКОЙ
VOLUME ./src
#VOLUME ["type=bind", "source=./src", "target=/nginx/app/static"]
#VOLUME [type: "bind", source: "./src", target: "/opt/app/static"]

