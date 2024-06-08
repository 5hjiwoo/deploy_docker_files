FROM openjdk:17
USER root

COPY sources.list /etc/apt/sources.list
RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install git -y
RUN git clone https://github.com/5hjiwoo/deploy_practice.git