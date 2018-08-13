FROM gcr.io/google_containers/kube-apiserver-amd64:v1.11.1
ENV TZ=Asia/Shanghai
RUN echo ' \
           deb http://mirrors.aliyun.com/debian/ stretch main non-free contrib \
          deb-src http://mirrors.aliyun.com/debian/ stretch main non-free contrib \
          deb http://mirrors.aliyun.com/debian-security stretch/updates main \
          deb-src http://mirrors.aliyun.com/debian-security stretch/updates main \
          deb http://mirrors.aliyun.com/debian/ stretch-updates main non-free contrib \
          deb-src http://mirrors.aliyun.com/debian/ stretch-updates main non-free contrib \
           deb http://mirrors.aliyun.com/debian/ stretch-backports main non-free contrib \
          deb-src http://mirrors.aliyun.com/debian/ stretch-backports main non-free contrib' > /etc/apt/sources.list
          && apt-get update
          && apt-get install tzdata
          && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
