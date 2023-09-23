# RustOS

A minimal operating system in Rust

## Setting up toolchain
```bash
rustup override set nightly
rustup component add rust-src
rustup component add llvm-tools-preview
cargo install bootimage
```

## Building
```bash
cargo bootimage --target x86_64-rust_os.json
```

## Booting with QEMU
```bash
qemu-system-x86_64 -drive format=raw,file=target/x86_64-rust_os/debug/bootimage-rust-os.bin
```
