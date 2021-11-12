SHELL := /bin/bash

.PHONY: help
help:
	@echo "available targets -->\n"
	@cat Makefile | grep ".PHONY" | grep -v ".PHONY: _" | sed 's/.PHONY: //g'


.PHONY: build-podman
build-podman:
	podman build . -t daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')


.PHONY: tag-podman
tag-podman: build-podman
	podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')-$$(uname -m)
	podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}')-$$(uname -m)
	podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}')-$$(uname -m)
	podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:latest-$$(uname -m)
	@echo podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')-$$(uname -m)
	@echo podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}')-$$(uname -m)
	@echo podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}')-$$(uname -m)
	@echo podman tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:latest-$$(uname -m)


.PHONY: push-podman
push-podman: tag-podman
	podman push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')-$$(uname -m)
	podman push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}')-$$(uname -m)
	podman push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}')-$$(uname -m)
	podman push docker.io/daxxog/castlecms:latest-$$(uname -m)



.PHONY: build-docker
build-docker:
	docker build . -t daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')


.PHONY: tag-docker
tag-docker: build-docker
	docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')-$$(uname -m)
	docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}')-$$(uname -m)
	docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}')-$$(uname -m)
	docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:latest-$$(uname -m)
	@echo docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')-$$(uname -m)
	@echo docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}')-$$(uname -m)
	@echo docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}')-$$(uname -m)
	@echo docker tag daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}') \
		docker.io/daxxog/castlecms:latest-$$(uname -m)


.PHONY: push-docker
push-docker: tag-docker
	docker push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')-$$(uname -m)
	docker push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}')-$$(uname -m)
	docker push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}')-$$(uname -m)
	docker push docker.io/daxxog/castlecms:latest-$$(uname -m)


.PHONY: create-manifest-docker
create-manifest-docker:
	pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}' | tee TAG
	cat <(echo set -x) <(echo docker manifest create "docker.io/daxxog/castlecms:$$(cat TAG) \\") <(cat UNAME_M | sed "s/^/--amend docker.io\/daxxog\/castlecms:$$(cat TAG)-/g; s/$$/ \\\/g") <(echo ';') | bash
	pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | tee TAG
	cat <(echo set -x) <(echo docker manifest create "docker.io/daxxog/castlecms:$$(cat TAG) \\") <(cat UNAME_M | sed "s/^/--amend docker.io\/daxxog\/castlecms:$$(cat TAG)-/g; s/$$/ \\\/g") <(echo ';') | bash
	pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}' | tee TAG
	cat <(echo set -x) <(echo docker manifest create "docker.io/daxxog/castlecms:$$(cat TAG) \\") <(cat UNAME_M | sed "s/^/--amend docker.io\/daxxog\/castlecms:$$(cat TAG)-/g; s/$$/ \\\/g") <(echo ';') | bash
	printf latest | tee TAG
	cat <(echo set -x) <(echo docker manifest create "docker.io/daxxog/castlecms:$$(cat TAG) \\") <(cat UNAME_M | sed "s/^/--amend docker.io\/daxxog\/castlecms:$$(cat TAG)-/g; s/$$/ \\\/g") <(echo ';') | bash
	rm TAG


.PHONY: push-manifest-docker
push-manifest-docker: create-manifest-docker
	docker manifest push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[3]}')
	docker manifest push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}')
	docker manifest push docker.io/daxxog/castlecms:$$(pwd | awk '{split($$0,a,"castle.docker");print a[2]}' | awk '{split($$0,a,"/");print a[2]}' | awk '{split($$0,a,".");print a[1]}')
	docker manifest push docker.io/daxxog/castlecms:latest
