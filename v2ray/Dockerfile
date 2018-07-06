#
# Dockerfile for v2ray
#

FROM golang:latest
MAINTAINER chanfried.chung <chanfried.chung@gmail.com>

ADD https://storage.googleapis.com/v2ray-docker/v2ray /usr/bin/v2ray/
ADD https://storage.googleapis.com/v2ray-docker/v2ctl /usr/bin/v2ray/
ADD https://storage.googleapis.com/v2ray-docker/geoip.dat /usr/bin/v2ray/
ADD https://storage.googleapis.com/v2ray-docker/geosite.dat /usr/bin/v2ray/
COPY config.json /etc/v2ray/config.json
RUN mkdir /var/log/v2ray/ &&\
    chmod a+x /usr/bin/v2ray/v2ctl && \
    chmod a+x /usr/bin/v2ray/v2ray
ENV PATH /usr/bin/v2ray:$PATH
CMD ["v2ray", "-config=/etc/v2ray/config.json"]

