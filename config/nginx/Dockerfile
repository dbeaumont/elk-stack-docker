# FROM nginx:1.9
FROM nginx:1.15.12

RUN apt-get update && apt-get install -y curl

# FIX expired key for GPG
# RUN curl -O https://nginx.org/keys/nginx_signing.key && apt-key add ./nginx_signing.key

HEALTHCHECK CMD curl -f http://localhost/server-status
COPY ./nginx.conf /etc/nginx/


