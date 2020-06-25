LATEST := 1.14.4-v0

latest:
	docker build -t dev-go:$(LATEST) -t dev-go:latest  \
		--build-arg go_version=1.14.4-alpine3.12@sha256:6042b9cfb4eb303f3bdcbfeaba79b45130d170939318de85ac5b9508cb6f0f7e \
		--build-arg protobuf_version=3.12.2-r0 \
		--build-arg protoc_gen_version=v1.4.2 \
		--build-arg make_version=4.3-r0 \
		.