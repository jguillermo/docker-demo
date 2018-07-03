.DEFAULT_GOAL := help

hello-world:## hola mundo en docker: make hello-world
	docker run hello-world 

pull:## bajar imagenes: make pull
	docker pull ubuntu

ubuntu:## ejecutar la imagen de ubuntu : make ubuntu
	docker run -it ubuntu bash

aws-image:## ejecutar la imagen de aws : make aws-image
	docker run -it amazonlinux:2018.03 bash

## Target Help ##
help:
	@printf "\033[31m%-16s %-59s %s\033[0m\n" "Target" "Help" "Usage"; \
	printf "\033[31m%-16s %-59s %s\033[0m\n" "------" "----" "-----"; \
	grep -hE '^\S+:.*## .*$$' $(MAKEFILE_LIST) | sed -e 's/:.*##\s*/:/' | sort | awk 'BEGIN {FS = ":"}; {printf "\033[32m%-16s\033[0m %-58s \033[34m%s\033[0m\n", $$1, $$2, $$3}'
	