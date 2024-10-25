.PHONY: build run destroy

build:
	@echo "Build the Images"
	docker build -t cars:v1 .
	docker build -t bikes:v1 .
	docker build -t yachts:v1 .

destroy:
	@echo "Destroy the images"
	docker rmi cars:v1 
	docker rmi bikes:v1 
	docker rmi yachts:v1

run:
	@echo "Run Containers with Compose"
	docker compose up -d --build
