FROM fedora
WORKDIR /usr/src/app

RUN dnf install php php-mysqli composer -y

COPY composer.json ./

RUN composer install --no-plugins --no-scripts

COPY . .

EXPOSE 5000
CMD [ "composer", "start"]