
# Dockerfile for xray based alpine
# Copyright (C) 2019 - 2021 TG:@Marscx
# Reference URL:
# https://github.com/crossfw/Air-Universe/releases

FROM alpine:latest
LABEL maintainer="marscx"
WORKDIR /root
COPY au /usr/bin/
RUN set -ex \
        && apk add --no-cache tzdata ca-certificates \
        && mkdir -p /var/log/au /usr/share/au \
    && chmod +x /usr/bin/au

VOLUME /etc/au
ENV TZ=Asia/Shanghai
CMD [ "/usr/bin/au", "-c", "/etc/au/au.json" ]
