FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends gdb python3-pip

RUN pip3 install online-judge-verify-helper

RUN git clone https://github.com/atcoder/ac-library.git -b v1.5.1 /opt/ac-library

ENV CPLUS_INCLUDE_PATH=/opt/ac-library:/workspaces/cp-container/libraries${CPLUS_INCLUDE_PATH:+:$CPLUS_INCLUDE_PATH}
