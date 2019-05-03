FROM mysql:5.7.12

# FIX
RUN printf "deb http://archive.debian.org/debian/ jessie main\ndeb-src http://archive.debian.org/debian/ jessie main\ndeb http://security.debian.org jessie/updates main\ndeb-src http://security.debian.org jessie/updates main" > /etc/apt/sources.list
RUN apt-key adv --keyserver pgp.mit.edu --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
RUN apt-get upgrade && apt-get update

COPY ./conf-file.cnf /etc/mysql/conf.d/conf-file.cnf
RUN apt-get update && apt-get install -y netcat
HEALTHCHECK CMD nc -z localhost 3306