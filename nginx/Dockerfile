#
# Nginx Dockerfile
#

# Pull base image.
FROM ubuntu:14.04

MAINTAINER Hans J Schroeder "https://github.com/dvbportal"

# install nginx
RUN \
  export DEBIAN_FRONTEND=noninteractive && \
  apt-get update && apt-get install -y nginx 

# Data volume for configuration
VOLUME ["/etc/nginx"]

# use standard ssl port
EXPOSE 443

# set command
CMD ["/usr/sbin/nginx"]
