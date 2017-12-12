DOCKER_IMAGE := ympons/circleci-node

# Build docker image.
build:
	docker build -t "$(DOCKER_IMAGE)" .
.PHONY: build

# Run bash in the image.
shell: build
	docker run --rm -it $(DOCKER_IMAGE) bash
.PHONY: shell

# Publish image to the Docker Hub.
publish: build
	docker push $(DOCKER_IMAGE)
.PHONY: publish