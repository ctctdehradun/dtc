FROM ubuntu:12.04
MAINTAINER Elliot Crosby-McCullough "elliot@smart-casual.com"

RUN apt-get install -y python-software-properties
RUN add-apt-repository ppa:webupd8team/java
RUN apt-get -qq update

RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN apt-get install -y oracle-java7-installer

RUN rm -rf /var/cache/oracle-jdk7-installer
