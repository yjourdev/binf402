#!/bin/bash
Binf: check createDirectories docker.io dockerImage write

check:
	@if ! [ "$(shell id -u)" = 0 ];then \
	echo "You are not root, run this target as root please";\
	exit 1; \
	fi

createDirectories:
	@mkdir -p  ~/docker
	@mkdir -p ~/docker/binff402
	@mkdir -p ~/docker/binff402/practical
docker.io:
	@apt install docker.io
dockerImage:
	@docker build -t binf:v0.1 .
write:
	@echo alias runDockerBinf=\'docker run -it -v ~/docker/binff402/practical:/practical binf:v0.1\' >> ~/.bashrc
