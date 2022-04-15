FROM debian:buster-slim

LABEL maintainer="hello@unately.com"
LABEL org.opencontainers.image.source https://github.com/unately/cogwheels
LABEL org.opencontainers.image.description The headless version 17 of eclipse-temurin 

RUN apt-get -qq update && \
    apt-get -qq -y --no-install-recommends install gnupg software-properties-common && \
    apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0x219BD9C9 && \
    apt-add-repository "deb http://repos.azul.com/azure-only/zulu/apt stable main" && \
    apt-get -qq update && \
    apt-get -qq -y dist-upgrade && \
    apt-get -qq -y --no-install-recommends install zulu-8-azure-jre-headless=8.58.0.13* && \
    apt-get -qq -y purge gnupg software-properties-common && \
    apt -y autoremove && \
    rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME=/usr/lib/jvm/zre-hl-8-azure-amd64