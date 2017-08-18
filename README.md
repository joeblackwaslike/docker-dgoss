# Dgoss Test Image
[![Build Status](https://travis-ci.org/joeblackwaslike/docker-dgoss.svg?branch=master)](https://travis-ci.org/joeblackwaslike/docker-dgoss) [![Docker Pulls](https://img.shields.io/docker/pulls/joeblackwaslike/dgoss.svg)](https://hub.docker.com/r/joeblackwaslike/dgoss/)


## Maintainer
Joe Black | <me@joeblack.nyc> | [github](https://github.com/joeblackwaslike)


## Introduction
This container contains [goss](https://github.com/aelsabbahy/goss) and [dgoss](https://github.com/aelsabbahy/goss/tree/master/extras/dgoss) for testing docker containers


## Using this image
*See [examples](examples)*

1. Copy the `tests` directory to the base of your repository.
2. Follow directions for dgoss, substituting `dgoss edit` and `dgoss run` with
   `tests/edit` and `tests/run` respectively.
3. Set your Makefile `test` target to `tests/run <docker run arguments>`
4. `make test`
