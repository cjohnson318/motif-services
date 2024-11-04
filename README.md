# Motif Services

This is a proof of concept for running a Python gRPC server. The idea is that
this server would run parameterized models and deliver results back to an HTTP
server running elsewhere.

## Install protobuf

```bash
brew install protobuf
```

## Python Environment

Create a virtual environment,

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Protoc Code Generation

Run `bash create-proto.bash` from the command line to regenerate protobuf
helper code.

## Using Docker

```bash
docker build -t motif-grpc-server .
docker run -it -p 50051:50051 motif-grpc-server
```
