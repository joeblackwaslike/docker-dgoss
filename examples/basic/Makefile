SHELL := /bin/bash

DOCKER_ORG ?= joeblackwaslike
DOCKER_REPO := dgoss-basic-example
DOCKER_TAG := latest
DOCKER_IMAGE := $(DOCKER_ORG)/$(DOCKER_REPO):$(DOCKER_TAG)

.PHONY: all build build-test templates test push-image

all: build test

build:
	docker build --force-rm -t $(DOCKER_IMAGE) .

build-tests:
	tests/edit $(DOCKER_IMAGE) tail -f /dev/null

test:
	tests/run $(DOCKER_IMAGE) tail -f /dev/null

push-image:
	if [[ $(TRAVIS) == 'true' ]]; then \
		docker login -u $(DOCKER_USER) -p $(DOCKER_PASS); \
	fi
	docker push $(DOCKER_IMAGE)
