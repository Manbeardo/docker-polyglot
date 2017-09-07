FROM debian:stable

RUN apt-get update && apt-get install -y \
  build-essential \
  git \
  bash \
  openssl \
  gnupg \
  curl \
  apt-transport-https

COPY gpg-keys /gpg-keys
COPY apt-sources/* /etc/apt/sources.list.d/
RUN apt-key add /gpg-keys/*

RUN apt-get update && apt-get install -y \
  openjdk-8-jdk \
  nodejs \
  yarn \
  docker-ce \
  jq \
  python-pip \
  openssh-client

RUN pip install --upgrade pip && pip install awscli --upgrade
