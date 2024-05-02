
# Use the CentOS 7 base image
FROM centos:7

# Install Apache HTTP Server
RUN yum -y update && yum -y install httpd && yum clean all

# Create mobile directory inside /var/www/html
RUN mkdir -p /var/www/html/mobile
WORKDIR /var/www/html
COPY index.html mobile/
COPY app_logo.png mobile/
COPY mobile_screenshot1.png mobile/
COPY mobile_screenshot2.png mobile/
COPY download_button.png mobile/
RUN echo "ServerName localhost" >> /etc/httpd/conf/httpd.conf
EXPOSE 80
CMD ["httpd", "-D", "FOREGROUND"]
