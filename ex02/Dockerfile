FROM ubuntu

RUN apt-get update
RUN apt-get install -y nginx

WORKDIR /usr/share/nginx/html

COPY ./webapp/index.html ./index.nginx-debian.html

ENTRYPOINT [ "nginx", "-g", "daemon off;" ]