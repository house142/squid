FROM node:latest
MAINTAINER hojin jun hojin.jun@house142.com

COPY ./frontend /app

WORKDIR /app
RUN npm install

COPY ./docker/node/local/start.sh /start.sh

RUN sed -i 's/\r//' /start.sh \
    && chmod +x /start.sh