FROM httpd:2.4.20

# FIX
RUN printf "deb http://archive.debian.org/debian/ jessie main\ndeb-src http://archive.debian.org/debian/ jessie main\ndeb http://security.debian.org jessie/updates main\ndeb-src http://security.debian.org jessie/updates main" > /etc/apt/sources.list

RUN apt-get update && apt-get install -y curl
HEALTHCHECK CMD curl -f http://localhost
COPY ./httpd.conf /usr/local/apache2/conf/httpd.conf