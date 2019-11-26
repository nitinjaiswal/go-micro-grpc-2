// vessel-service/Makefile
build:
	protoc -I. --go_out=plugins=micro:. \
      proto/vessel/vessel.proto
	docker build -t docker-vessel-service .

run:
	docker run -p 50052:50051 -e MICRO_SERVER_ADDRESS=:50051 docker-vessel-service
