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




