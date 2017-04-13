FROM ubuntu:trusty
MAINTAINER Paweł Jasiak <pj1031999@gmail.com>

RUN apt-get update && apt-get install -y  \
    gcc \
    g++ \
    gcc-multilib \
    g++-multilib \
    build-essential \
    vim \
    valgrind    \
    gdb \
    fpc \
    libc6-dev   \
    unzip   \
    wget    \
    --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

RUN wget -O oitimetool.zip https://github.com/olimpiada/oitimetool-bin/archive/master.zip \
    && unzip oitimetool.zip \
    && wget  http://software.intel.com/sites/landingpage/pintool/downloads/pin-2.14-71313-gcc.4.4.7-linux.tar.gz \
    && tar xf pin-2.14-71313-gcc.4.4.7-linux.tar.gz \
    && rm pin-2.14-71313-gcc.4.4.7-linux.tar.gz \
    && mv pin-2.14-71313-gcc.4.4.7-linux ./oitimetool-bin-master/


WORKDIR /root
ENTRYPOINT /bin/bash
