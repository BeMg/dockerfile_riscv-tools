FROM ubuntu:18.04
MAINTAINER BeMg

RUN apt-get update && apt-get install -y git autoconf automake autotools-dev curl libmpc-dev libmpfr-dev libgmp-dev libusb-1.0-0-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev device-tree-compiler pkg-config libexpat-dev
RUN git clone https://github.com/riscv/riscv-tools.git && mkdir risc-v
ENV RISCV /risc-v
RUN cd riscv-tools && git submodule update --init --recursive && ./build.sh && cd / && rm -rf riscv-tools && echo "export PATH=$PATH:/risc-v/bin" >> ~/.bashrc