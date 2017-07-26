FROM debian:stable

RUN apt-get update && apt-get install -y \
  build-essential \
  git \
  bash \
  openssl \
  gnupg \
  curl \
  apt-transport-https

COPY yarn.pubkey.gpg /
COPY yarn.list /etc/apt/sources.list.d/
RUN apt-key add /yarn.pubkey.gpg

RUN apt-get update && apt-get install -y \
  openjdk-8-jdk \
  yarn
