# ruby and node.js

|name|description|
|:--|:-----------|
|OS|alpine linux|
|ruby|2.3.1|
|node|6.3.1|

## Using images

```
$ docker pull pyar6329/ruby-node:2.3.1-6.3.1
```

[https://hub.docker.com/r/pyar6329/ruby-node/](https://hub.docker.com/r/pyar6329/ruby-node/)

### Using C-based gems


```
ARG BUILD_PACKAGES="openssl-dev bash ca-certificates wget curl-dev build-base alpine-sdk"
ARG DEV_PACKAGES="ruby-dev zlib-dev libxml2-dev libxml2-utils libxslt-dev tzdata yaml-dev readline-dev sqlite-dev postgresql-dev mysql-dev"

RUN set -x \
    && apk add --update --upgrade --no-cache --virtual .build-packages $BUILD_PACKAGES \
    && apk add --update --upgrade --no-cache --virtual .dev-packages $DEV_PACKAGES
```
