#!/bin/bash
Binf: createDirectories docker.io dockerImage write

createDirectories:
	@mkdir -p ~/docker
	@mkdir -p ~/docker/binff402
	@mkdir -p ~/docker/binff402/practical
docker.io:
	@sudo apt install docker.io
dockerImage:
	@docker build -t binf:v0.1 .
write:
	@echo alias runDockerBinf=\'docker run -it -v ~/docker/binff402/practical:/practical binf:v0.1\' >> ~/.bashrc
