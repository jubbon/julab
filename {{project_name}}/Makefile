IMAGE_NAME={{ project_name }}-jupyter
IMAGE_TAG=latest
NB_USER=${shell whoami}
NB_UID=${shell id -u}
NB_GID=${shell id -g}


.PHONY: build up down


build:
	@(NB_USER=${NB_USER} NB_UID=${NB_UID} NB_GID=${NB_GID} IMAGE_NAME=${IMAGE_NAME} IMAGE_TAG=${IMAGE_TAG} docker-compose --file docker/docker-compose.yaml build)

up:
	@(NB_USER=${NB_USER} NB_UID=${NB_UID} NB_GID=${NB_GID} IMAGE_NAME=${IMAGE_NAME} IMAGE_TAG=${IMAGE_TAG} docker-compose --file docker/docker-compose.yaml up -d)

down:
	@(NB_USER=${NB_USER} NB_UID=${NB_UID} NB_GID=${NB_GID} IMAGE_NAME=${IMAGE_NAME} IMAGE_TAG=${IMAGE_TAG} docker-compose --file docker/docker-compose.yaml down)

