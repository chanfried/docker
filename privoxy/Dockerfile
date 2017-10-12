#
# Dockerfile for privoxy
#

FROM alpine:latest
MAINTAINER kev <chanfried.chung@gmail.com>

RUN apk --no-cache add privoxy \
    && rm -rf /var/cache/apk/*

VOLUME /etc/privoxy

EXPOSE 8118

CMD privoxy --no-daemon /etc/privoxy/config

