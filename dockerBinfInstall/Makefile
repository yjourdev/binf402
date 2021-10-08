#!/bin/bash
Binf: createDirectories docker.io dockerImage write

createDirectories:
	@mkdir  ~/docker
	@mkdir ~/docker/binff402
	@mkdir ~/docker/binff402/practical
docker.io:
	@apt install docker.io
dockerImage:
	@docker build -t binf:v0.1 .
write:
	@echo alias runDockerBinf=\'docker run -it -v ~/docker/binff402/practical:/practical binf:v0.1\' >> ~/.bashrc
