# docker-go

[![Docker Repository on Quay](https://quay.io/repository/hyper/go/status "Docker Repository on Quay")](https://quay.io/repository/hyper/go)
[![Docker Build Status](https://img.shields.io/docker/build/hyperjiang/golang.svg)](https://hub.docker.com/r/hyperjiang/golang)
[![Docker Pulls](https://img.shields.io/docker/pulls/hyperjiang/golang.svg)](https://hub.docker.com/r/hyperjiang/golang)
[![License](https://img.shields.io/github/license/hyperjiang/docker-go.svg)](https://github.com/hyperjiang/docker-go)

Docker image for golang which contains:

- [GoMock](https://github.com/golang/mock)
- [Protocol Buffers](https://github.com/protocolbuffers/protobuf)
- [Protocol Buffers for Go with Gadgets](https://github.com/gogo/protobuf)
- [Golang ProtoBuf Validator Compiler](https://github.com/mwitkow/go-proto-validators)
- [gRPC-Go](https://github.com/grpc/grpc-go)
- [gRPC Gateway](https://github.com/grpc-ecosystem/grpc-gateway)
- [prototool](https://github.com/uber/prototool)

## pull the docker image

For newer images (version >= 1.13)

```
docker pull hyperjiang/golang
```

or

```
docker pull quay.io/hyper/go
```

For legacy images (version <= 1.12.9)

```
docker pull hyperjiang/golang
```

Latest versions:

- lastest, 1.14, 1.14.4
- 1.13, 1.13.12

Check more available versions here: https://github.com/hyperjiang/docker-go/releases

## breaking changes

From 1.13 and later on, [dep](https://github.com/golang/dep) is removed from the images.

From 1.13.5 and 1.12.14 and later on, [buf](https://github.com/bufbuild/buf) and [prototool](https://github.com/uber/prototool) are pre-installed.

From 1.14.2 and later on, [buf](https://github.com/bufbuild/buf) is removed as it does not support 1.14.

## unbuilt versions

Some golang versions have defects, so their images will not be built.

- 1.11.3 and 1.10.6 have a bug which will break "go get" for import path patterns containing "..."
- 1.11.7, 1.11.8, 1.12.2, 1.12.3 have a bug of using the prebuilt binary releases on older versions of GNU/Linux led to failures when linking programs that used cgo.
- 1.12.8 has bugs in linker and the os and math/big package.
- 1.12.11, 1.13.2 has bugs in go command, runtime, syscall and net packages.
