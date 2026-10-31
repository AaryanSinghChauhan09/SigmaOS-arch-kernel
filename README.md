# SigmaOS Arch Kernel Inspirations

A Rust library collecting kernel and Arch Linux inspired mechanisms, including a KUnit-style expectation runner, package transaction and dependency models, advisory tracking, signing policy models, initramfs hook configuration, rebuild ordering, package signoff, and reproducible-build records.

These are in-process models and prototypes. They are not a replacement for Linux KUnit, pacman/ALPM, a cryptographic signing backend, a security advisory service, or a real initramfs/build pipeline. In particular, the source currently uses `std`; despite an introductory source comment, this crate is not `no_std` as written.

## Build

The manifest references the sibling [`SigmaOS-kernel`](../SigmaOS-kernel) crate by path. From the SigmaOS checkout:

```sh
cargo check --manifest-path SigmaOS-arch-kernel/Cargo.toml --lib
```

## License

GPL-3.0-or-later. See [`Cargo.toml`](Cargo.toml).
