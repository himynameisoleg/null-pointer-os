# null-pointer-os

An implementation of a simple operating system kernel written in Rust for bare metal.

Base on the blog series [Writing an OS in Rust](https://os.phil-opp.com/).

## Building

```bash
# Build to specific target
cargo build --target thumbv7em-none-eabihf

# Build based on predfined targets in .cargo/config
cargo build
```

## Running bootable image in QEMU

```bash
# add the following as prerequisites
cargo install bootimage
rustup component add llvm-tools-preview

# create bootable disk iamge by running
cargo bootimage

# run the bootable image using QEMU
qemu-system-x86_64 -drive format=raw,file=target/x86_64-blog_os/debug/bootimage-blog_os.bin
```

Subsequent runs can be run with `cargo run`.
