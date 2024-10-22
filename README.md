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
