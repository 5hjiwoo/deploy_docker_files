FROM ubuntu:20.04

ENV JDK_MAJOR_VERSION 17

RUN apt-get update && \
    apt-get install -y gnupg ca-certificates curl && \
    curl -s https://repos.azul.com/azul-repo.key | gpg --dearmor -o /usr/share/keyrings/azul.gpg && \
    echo "deb [signed-by=/usr/share/keyrings/azul.gpg] https://repos.azul.com/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list && \
    apt-get update && \
    apt-get install -y zulu17-jdk && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME /usr/lib/jvm/zulu17-ca-amd64
USER root

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install git -y
RUN git clone https://github.com/5hjiwoo/deploy_practice.git