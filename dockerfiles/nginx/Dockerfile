FROM nginx:1.17-alpine

RUN apk --update add tzdata openssl && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del tzdata && \
    rm -rf /var/cache/apk/*
