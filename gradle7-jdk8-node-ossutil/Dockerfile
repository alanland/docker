FROM gradle:7.1.1-jdk8

## https://github.com/docker-library/openjdk
## https://github.com/docker-library/openjdk/tree/dd54ae37bc44d19ecb5be702d36d664fed2c68e4
# https://pkgs.alpinelinux.org/package/edge/community/x86/openjdk8-jre

COPY ../sources.list  /etc/apt/sources.list
RUN apt-get update -yq \
    && apt-get install curl gnupg -yq \
    && curl -sL https://deb.nodesource.com/setup_12.x | bash \
    && apt-get install nodejs yarn -yq \
    && curl --output /usr/local/bin/ossutil "https://ttx-download.oss-cn-hangzhou.aliyuncs.com/aliyun/ossutil/ossutil64" \
    && chmod +x /usr/local/bin/ossutil \
    && echo "Clean cache" \
    && rm -rf /var/lib/apt/lists/*
