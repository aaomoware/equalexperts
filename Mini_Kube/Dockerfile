FROM centos:centos7

MAINTAINER aaomoware

RUN yum install ruby httpd -y
RUN yum clean all

COPY hw.rb /tmp/hw.rb

RUN ruby /tmp/hw.rb > /var/www/html/index.html

EXPOSE 80
ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
