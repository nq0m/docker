FROM centos:latest

MAINTAINER Jeremy Utley "jerutley@gmail.com"

RUN yum clean all && yum -y update

RUN yum -y install epel-release

RUN yum -y --nogpgcheck install http://rpms.remirepo.net/enterprise/remi-release-7.rpm

RUN yum -y install yum-utils

RUN yum-config-manager --enable remi-php56

RUN yum -y install \
    php \
    php-bcmath \
    php-common \
    php-fpm \
    php-gd \
    php-imap \
    php-ldap \
    php-mbstring \
    php-mcrypt \
    php-mysqlnd \
    php-odbc \
    php-pdo \
    php-process \
    php-recode \
    php-snmp \
    php-tidy \
    php-xml \
    php-xmlrpc

EXPOSE 9000

CMD ["/usr/sbin/php-fpm", "-F;"]
