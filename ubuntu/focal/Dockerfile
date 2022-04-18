FROM ubuntu:focal

LABEL maintainer="hello@unately.com"
LABEL org.opencontainers.image.source https://github.com/unately/cogwheels
LABEL org.opencontainers.image.description The Ubuntu Focal Version by unately

ENV DEBIAN_FRONTEND=noninteractive

RUN  dpkg --add-architecture i386 \
	 && apt update \
	 && apt dist-upgrade -y \
	 && apt -y --no-install-recommends install grep ca-certificates curl lib32gcc-s1 libsdl2-2.0-0:i386 git wget bash