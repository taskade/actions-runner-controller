NAME ?= 843776460877.dkr.ecr.us-east-1.amazonaws.com/taskade/actions-runner

RUNNER_VERSION ?= 2.267.1
DOCKER_VERSION ?= 19.03.8

docker-build:
	docker build --build-arg RUNNER_VERSION=${RUNNER_VERSION} --build-arg DOCKER_VERSION=${DOCKER_VERSION} -t ${NAME}:latest -t ${NAME}:v${RUNNER_VERSION} .

docker-build-ecr:
	docker build --build-arg RUNNER_VERSION=${RUNNER_VERSION} --build-arg DOCKER_VERSION=${DOCKER_VERSION} -t ${NAME}:20200723 .

docker-push:
	docker push ${NAME}:latest
	docker push ${NAME}:v${RUNNER_VERSION}
