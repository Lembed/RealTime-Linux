FROM ubuntu:14.04

# Install dependencies
RUN apt-get update               \
 && apt-get -y -q upgrade        \
 && apt-get -y -q install        \
    bc                           \
    binutils-arm-linux-gnueabihf \
    build-essential              \
    ccache                       \
    gcc-arm-linux-gnueabihf      \
    gccgo-4.7-arm-linux-gnueabi  \
    git                          \
    libncurses-dev               \
    libssl-dev                   \
    u-boot-tools                 \
    wget                         \
    xz-utils                     \
 && apt-get clean


# Install DTC
RUN wget http://ftp.fr.debian.org/debian/pool/main/d/device-tree-compiler/device-tree-compiler_1.4.0+dfsg-1_amd64.deb -O /tmp/dtc.deb \
 && dpkg -i /tmp/dtc.deb \
 && rm -f /tmp/dtc.deb


# Fetch the kernel
ENV LINUX_DIR=/opt/real_time_linux 

WORKDIR ${LINUX_DIR}
