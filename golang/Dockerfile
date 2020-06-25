# Base Golang Version
ARG go_version
FROM golang:$go_version
# Use go modules
ENV GO111MODULE=on
# Protobuf for gRPC
ARG protobuf_version
RUN apk add protobuf=$protobuf_version
ARG protoc_gen_version
RUN go get github.com/golang/protobuf/protoc-gen-go@$protoc_gen_version

# Add make capabilities
ARG make_version
RUN apk add make=$make_version
# Run as non-root user
RUN addgroup -S gogroup && adduser -S gouser -G gogroup
USER gouser
WORKDIR /home/gouser/dev