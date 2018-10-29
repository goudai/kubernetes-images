FROM alpine:3.8
MAINTAINER qingmu 247687009@qq.com
ENV LANG=C.UTF-8 \
    JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre \
    PATH=$PATH:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin \
    TZ=Asia/Shanghai
RUN echo "" > /etc/apk/repositories \
&& echo "https://mirrors.aliyun.com/alpine/v3.8/main/" >> /etc/apk/repositories \
&& echo "https://mirrors.aliyun.com/alpine/v3.8/community/" >> /etc/apk/repositories \
&& apk update && apk add --no-cache openjdk8-jre ca-certificates tzdata tini \
&& rm -rf /var/cache/apk/* \
&& ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone