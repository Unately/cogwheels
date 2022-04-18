FROM ubuntu:focal

LABEL maintainer="hello@unately.com"
LABEL org.opencontainers.image.source https://github.com/unately/cogwheels
LABEL org.opencontainers.image.description The Ubuntu Focal Version by unately

ENV DEBIAN_FRONTEND=noninteractive

RUN  dpkg --add-architecture i386 \
	 && apt-get update \
	 && apt-get dist-upgrade -y \
	 && apt-get -y --no-install-recommends install grep ca-certificates curl zip unzip openjdk-17-jre-headless lib32gcc-s1 libsdl2-2.0-0:i386 git wget bash dos2unix