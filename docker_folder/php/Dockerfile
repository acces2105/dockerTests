#FROM php:8.2-cli
FROM php:7.4-cli
RUN apt-get update
RUN apt-get install -y lsb-release ca-certificates apt-transport-https curl
RUN curl -sSLo /tmp/debsuryorg-archive-keyring.deb https://packages.sury.org/debsuryorg-archive-keyring.deb
RUN dpkg -i /tmp/debsuryorg-archive-keyring.deb
RUN sh -c 'echo "deb [signed-by=/usr/share/keyrings/debsuryorg-archive-keyring.gpg] https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'
RUN apt-get update
RUN apt install -y php7.4-fpm 

#COPY ./src  
#WORKDIR /src/myapp  
#CMD [ "php", "./index.php" ]  
#CMD ["php -a"]
#COPY . /usr/src/myapp
#WORKDIR /usr/src/myapp
#CMD [ "php", "./your-script.php" ]