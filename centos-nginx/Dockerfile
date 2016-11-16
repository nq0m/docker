FROM centos:latest

MAINTAINER Jeremy Utley "jerutley@gmail.com"

RUN yum clean all && yum -y update

RUN yum -y install epel-release

RUN yum -y install nginx

RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

RUN mkdir -p /srv/www

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
