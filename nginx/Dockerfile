# Nginx Dockerfile

FROM nginx:latest

RUN apt-get update
RUN apt-get install -y vim net-tools telnet curl  wget

RUN rm /etc/nginx/nginx.conf
RUN rm /etc/nginx/conf.d/default.conf


CMD ["nginx", "-g", "daemon off;"]
