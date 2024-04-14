## Dev rust in docker

This repo shows how to build rust inside docker image and cross compile to windows

```shell
docker-compose run --rm dev
```

### Cross compile for Windows

```shell
rustup target add x86_64-pc-windows-msvc
cargo install cargo-xwin
cargo xwin build --release --target x86_64-pc-windows-msvc
```