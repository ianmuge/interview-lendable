FROM alpine:3.8

RUN addgroup www
RUN adduser -D -g 'www' nginx
RUN mkdir -p /run/nginx

RUN apk update && apk add nginx curl

RUN mkdir /www && \
    chown -R nginx:www /var/lib/nginx && \
    chown -R nginx:www /www

COPY nginx/default.conf /etc/nginx/conf.d/default.conf
# COPY www/* /www/
EXPOSE 80
STOPSIGNAL SIGTERM
CMD ["nginx", "-g", "daemon off;"]