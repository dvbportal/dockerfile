#
# Python Dockerfile
#

# Pull base image.
FROM ubuntu:14.04

MAINTAINER Hans J Schroeder "https://github.com/dvbportal"

# Install python.
RUN \
  export DEBIAN_FRONTEND=noninteractive && \
  apt-get update && \
  apt-get install -y python python-dev python-pip python-virtualenv wget && \
  rm -rf /var/lib/apt/lists/*

# Define working directory.
WORKDIR /data

# Define default command.
CMD ["bash"]
