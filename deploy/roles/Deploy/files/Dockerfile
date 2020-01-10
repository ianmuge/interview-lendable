FROM alpine:3.8

RUN addgroup www
RUN adduser -D -g 'www' nginx

RUN apk update && apk add nginx

RUN mkdir /www && \
    chown -R nginx:www /var/lib/nginx && \
    chown -R nginx:www /www

COPY nginx/default.conf /etc/nginx/conf.d/default.conf

ENTRYPOINT nginx -g 'daemon off;'