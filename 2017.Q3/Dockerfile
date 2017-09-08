FROM debian:stable

# stuff we need to add other repos
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

# platforms
RUN apt-get update && apt-get install -y \
  openjdk-8-jdk \
  nodejs \
  yarn \
  docker-ce \
  jq \
  python-pip

# misc tools
RUN apt-get update && apt-get install -y \
  openssh-client \
  vim

RUN pip install --upgrade pip && pip install awscli --upgrade
