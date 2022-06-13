
ARG VERSION=20.04

FROM ubuntu:$VERSION

RUN apt-get update -y && apt-get install -y gnupg wget python3 python3-distro && \
    wget -qO - https://packages.irods.org/irods-signing-key.asc | apt-key add - && \
    echo "deb [arch=amd64] https://packages.irods.org/apt/ $(lsb_release -sc) main" >> /etc/apt/sources.list.d/renci-irods.list && \
    apt-get update && apt-get install irods-icommands -y

COPY irods_environment.json /home/ubuntu/.irods/

RUN useradd ubuntu && \
    chown -R ubuntu:ubuntu /home/ubuntu

USER ubuntu