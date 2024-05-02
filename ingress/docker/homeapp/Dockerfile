
# Use the CentOS 7 base image
FROM centos:7

# Install Apache HTTP Server
RUN yum -y update && yum -y install httpd && yum clean all

# Create home directory inside /var/www/html
RUN mkdir -p /var/www/html/home

# Set /var/www/html as the working directory
WORKDIR /var/www/html

# Copy the HTML and CSS files into the /var/www/html/home directory
COPY index.html home/
COPY styles.css home/
RUN echo "ServerName localhost" >> /etc/httpd/conf/httpd.conf
EXPOSE 80
CMD ["httpd", "-D", "FOREGROUND"]
