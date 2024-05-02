
FROM centos:7
RUN yum -y update && yum -y install httpd && yum clean all
RUN mkdir -p /var/www/html/home
WORKDIR /var/www/html
COPY index.html home/
COPY styles.css home/
RUN echo "ServerName localhost" >> /etc/httpd/conf/httpd.conf
EXPOSE 80
CMD ["httpd", "-D", "FOREGROUND"]
