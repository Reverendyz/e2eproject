FROM debian:latest

ENV MINNAKER_VERSION=0.1.3
ENV PRIVATE_IP=192.168.15.250
ENV VERSION=v4.2.0
ENV BINARY=yq_linux_amd64

RUN apt-get update && apt-get install -y curl git tar

RUN curl -sL "https://github.com/armory/minnaker/archive/v${MINNAKER_VERSION}.tar.gz" -o minnaker.tar.gz && \
    tar zxvf minnaker.tar.gz

WORKDIR "/minnaker-${MINNAKER_VERSION}"

RUN ./scripts/install.sh
