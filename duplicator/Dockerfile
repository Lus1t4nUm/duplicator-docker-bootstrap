FROM yobasystems/alpine-php-wordpress
WORKDIR /usr/html
COPY ./content/* ./
RUN apk update
RUN apk add --upgrade apk-tools
RUN apk upgrade --available
RUN sync
RUN reboot
