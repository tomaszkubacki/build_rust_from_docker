# Dev rust in docker

This repo shows how to build rust inside docker image and cross compile to windows

## run docker image with rust 

```shell
docker-compose run --rm rust_builder
```

## cross compile for Windows

install dependencies

```shell
sudo apt-get install cmake mingw-w64
rustup target add x86_64-pc-windows-gnu
```

build with target Windows

```shell
cargo build --target x86_64-pc-windows-gnu -r
```

## clean up 

```shell
docker rmi rust-builder
```
