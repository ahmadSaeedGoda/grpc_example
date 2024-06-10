# gRPC Example with Go

This repository contains a simple example of using gRPC with Go, including both the server and client code. The example demonstrates how to define a service with Protocol Buffers, generate Go code from the `.proto` file, and implement the server and client.

## Prerequisites

- Go 1.16 or higher
- Protocol Buffers Compiler (`protoc`)
- Go plugins for Protocol Buffers (`protoc-gen-go` and `protoc-gen-go-grpc`)

## Installation

### 1. Install Protocol Buffers Compiler

#### macOS
```sh
brew install protobuf
```

#### Linux/Ubuntu
```sh
sudo apt install -y protobuf-compiler
```

Make sure $GOPATH/bin is in your PATH to access the installed binaries:

```sh
export PATH="$PATH:$(go env GOPATH)/bin"
```

#### Install Dependencies
```sh
go mod tidy
```

#### Run the Server and Client
```sh
go run server/server.go
```
In a separate terminal, run the client:
```sh
go run client/client.go <your-name-e.g.>
```
You should see the server logs the name received from the client and the client log the greeting received from the server.
