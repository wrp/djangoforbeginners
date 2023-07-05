

image ?= chicory-auth

.PHONY: build run all
all: build run

run:
	docker run -p 8080:8080 "$(image)"

build:
	docker build . -t "$(image)"
