#
# Dockerfile for v2ray
#

FROM alpine:latest
MAINTAINER chanfried.chung <chanfried.chung@gmail.com>

ADD v2ray /usr/bin/v2ray/
ADD v2ctl /usr/bin/v2ray/
ADD geoip.dat /usr/bin/v2ray/
ADD geosite.dat /usr/bin/v2ray/
COPY config.json /etc/v2ray/config.json
RUN set -ex && \
    apk --no-cache add ca-certificates && \
    mkdir /var/log/v2ray/ &&\
    chmod +x /usr/bin/v2ray/v2ctl && \
    chmod +x /usr/bin/v2ray/v2ray
ENV PATH /usr/bin/v2ray:$PATH
CMD ["v2ray", "-config=/etc/v2ray/config.json"]

