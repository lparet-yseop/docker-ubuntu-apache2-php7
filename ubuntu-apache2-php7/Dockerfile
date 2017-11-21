FROM lparet/docker-ubuntu-apache2:1.2
LABEL Louis Paret <perso@louisparet.fr>

## Install packages
RUN apt-get update \
  && apt-get -y install \
    php \
    libapache2-mod-php \
    php-mcrypt \
    php-mysql \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

## CMD : Supervisor
CMD ["supervisord","-c","/etc/supervisord.conf"]
