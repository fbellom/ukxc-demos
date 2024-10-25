.PHONY: build run destroy
build:
	@echo "Building New Image"
	docker build -t my-node-app:latest .

run:
	@echo "Runing demo Container"
	docker run -p 3000:3000 --rm my-node-app

destroy:
	@echo "Destroy demo Image"
	docker image rm my-node-app

