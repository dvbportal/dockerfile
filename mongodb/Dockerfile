#
# MongoDB 3 Dockerfile
#

# Pull base image.
FROM ubuntu:14.04

MAINTAINER Hans J Schroeder "https://github.com/dvbportal"

# install mongodb
RUN \
  export DEBIAN_FRONTEND=noninteractive && \
  apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10 && \
  echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.0 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-3.0.list && \
  apt-get update && apt-get install -y mongodb-org

# Data volume for mongodb
VOLUME ["/data"]

RUN mkdir -p /data/db

# use standard mongodb port
EXPOSE 27017

# Set usr/bin/mongod as the dockerized entry-point application
ENTRYPOINT ["/usr/bin/mongod"]
