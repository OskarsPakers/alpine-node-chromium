FROM node:12-alpine

RUN \
  echo "http://dl-cdn.alpinelinux.org/alpine/v3.10/community" >> /etc/apk/repositories \
  && echo "@latestcommunity http://dl-cdn.alpinelinux.org/alpine/v3.10/community" >> /etc/apk/repositories \
  && apk --no-cache update \
  && apk --no-cache upgrade \
  && apk add --no-cache --virtual .build-deps gifsicle optipng libjpeg-turbo-utils udev chromium python py-pip make gcc g++ \
  && apk add --no-cache pngquant@latestcommunity ttf-opensans@latestcommunity \
  && rm -rf /var/cache/apk/* /tmp/*

ENV CHROME_BIN /usr/bin/chromium-browser
ENV LIGHTHOUSE_CHROMIUM_PATH /usr/bin/chromium-browser
