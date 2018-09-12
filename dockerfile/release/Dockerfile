FROM alpine

RUN apk --update add git

RUN cd / && git clone https://github.com/HaitaoYue/docker-auto-build.git app && \
	cd app && lastTag=$(git describe --tags `git rev-list --tags --max-count=1`) && \
	git checkout -b $lastTag $lastTag
