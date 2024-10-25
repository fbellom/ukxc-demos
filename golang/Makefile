.PHONY:	build run destroy init refresh

build:
	@echo "build the container"
	docker build -t my-golang-app .

run:
	@echo "Runing demo Container"
	docker run -p 8001:8001 --rm my-golang-app

destroy:
	@echo "Destroy Image"
	docker image rm my-golang-app

init:
	build
	run

refresh:
	destroy
	build
	run



