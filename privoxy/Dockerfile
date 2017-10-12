#
# Dockerfile for privoxy
#

FROM alpine:latest
MAINTAINER kev <chanfried.chung@gmail.com>

RUN apk --no-cache add privoxy \
    && rm -rf /var/cache/apk/*

RUN sed -i -e '/^listen-address/s/127.0.0.1/0.0.0.0/' \
           -e '/^accept-intercepted-requests/s/0/1/' \
           -e '/^enforce-blocks/s/0/1/' \
           -e '/^#debug/s/#//' /etc/privoxy/config

VOLUME /etc/privoxy

EXPOSE 8118

CMD privoxy --no-daemon /etc/privoxy/config