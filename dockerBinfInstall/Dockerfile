FROM ubuntu:20.04

# LABEL about the custom image

LABEL maintainer="youri.jourdevant@ulb.be"
LABEL version="0.1"
LABEL description="This is custom Docker Image for \
    binf403 cours"
ENV DEBIAN_FRONTEND=noninteractive
VOLUME practical
RUN apt update -y && apt upgrade -y
RUN apt install -y python3
RUN apt install -y minimap2
RUN apt install -y fastqc
RUN apt install -y skewer
RUN apt install -y miniasm
RUN apt install -y racon
RUN apt install -y cargo
RUN cargo install fpa_lr
RUN apt-get install -y libz-dev
RUN apt install -y unicycler
RUN apt install -y python3-pip
RUN apt install -y git
RUN cd /usr/local/bin
RUN export PATH="usr/local/bin:$PATH"
RUN pip3 install git+https://github.com/rrwick/Minipolish.git
RUN cd
VOLUME practical
RUN apt install -y cmake
RUN cd usr/local/bin &&\
 git clone https://github.com/lbcb-sci/raven &&\
 cd raven && mkdir build && cd build &&\
 cmake -DCMAKE_BUILD_TYPE=Release .. &&\
 make
ENV PATH="/usr/local/bin/raven/build/bin/:${PATH}"
RUN git clone https://github.com/fenderglass/Flye &&\
 cd Flye &&\
 python3 setup.py install
RUN apt install -y canu
RUN apt install -y curl
RUN apt install -y bedtools
RUN cd /usr/local/bin &&\ 
 git clone https://github.com/tseemann/barrnap.git
ENV PATH="/usr/local/bin/barrnap/bin:${PATH}"
RUN apt install -y prokka
