FROM nginx:1.29
RUN rm /etc/nginx/nginx.conf
COPY ./nginx.conf /etc/nginx/nginx.conf
RUN rm /etc/nginx/conf.d/default.conf
COPY ./sites-available/nginx_main_http.conf /etc/nginx/conf.d/nginx_main_http.conf
COPY ./src /