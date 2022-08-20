FROM node:17-alpine

ARG PROJECT_WORKDIR

RUN apk add --update \
    python3 \
    python3-dev \
    py-pip \
    build-base \
    git \
    openssh-client \
    optipng \
    autoconf \
    jpeg-dev \
    zlib-dev \
    automake \
    libtool \
    pkgconfig \
    rsync \
  && rm -rf /var/cache/apk/*

RUN npm install -g npm@latest

WORKDIR $PROJECT_WORKDIR

RUN chown -R root /var/www/project

EXPOSE 3000

CMD ["node"]
