FROM ubuntu:trusty
MAINTAINER Stanley Yeo <yyoud88@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

WORKDIR /tmp

RUN apt-get update && \
    apt-get install -y curl openjdk-6-jre-headless && \
    curl -sSfL http://downloads.mesosphere.io/master/ubuntu/14.04/mesos_0.19.1-1.0.ubuntu1404_amd64.deb --output /tmp/mesos.deb && \
    dpkg -i /tmp/mesos.deb
    apt-get install -f -y && \
    rm /tmp/mesos.deb && \
    apt-get clean
