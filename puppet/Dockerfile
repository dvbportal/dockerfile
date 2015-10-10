#
# Puppet Dockerfile
#

# Pull base image.
FROM ubuntu:14.04

MAINTAINER Hans J Schroeder "https://github.com/dvbportal"

# install puppet
RUN \
  export DEBIAN_FRONTEND=noninteractive && \
  apt-get update && apt-get install -y puppet

# Data volume for configuration
VOLUME ["/etc/puppet"]

# use standard ssl port
EXPOSE 8139

# set command
CMD ["/usr/bin/puppet", "agent", "--no-daemonize"]
