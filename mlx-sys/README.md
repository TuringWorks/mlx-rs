# mlx-sys-burn

[![Crates.io](https://img.shields.io/crates/v/mlx-sys-burn.svg)](https://crates.io/crates/mlx-sys-burn)
[![Documentation](https://docs.rs/mlx-sys-burn/badge.svg)](https://docs.rs/mlx-sys-burn)
[![License](https://img.shields.io/badge/license-MIT%2FApache--2.0-blue.svg)](LICENSE)

Low-level Rust FFI bindings to Apple's [mlx-c](https://github.com/ml-explore/mlx-c) API, generated using bindgen.

This is a fork of [mlx-sys](https://crates.io/crates/mlx-sys) published to enable [burn-mlx](https://crates.io/crates/burn-mlx) on crates.io.

## Overview

This crate provides:
- Raw FFI bindings to mlx-c (the C API for MLX)
- Build script that compiles mlx-c from source
- Automatic linking to Metal and Accelerate frameworks

## Installation

```toml
[dependencies]
mlx-sys-burn = "0.2.1"
```

## Feature Flags

| Feature | Default | Description |
|---------|---------|-------------|
| `metal` | Yes | Enable Metal GPU support |
| `accelerate` | Yes | Enable Accelerate framework for optimized CPU operations |

## Usage

This crate provides raw FFI bindings. You typically don't use it directly.

For a safe, idiomatic Rust interface, use [mlx-rs-burn](https://crates.io/crates/mlx-rs-burn):

```toml
[dependencies]
mlx-rs-burn = "0.25.4"
```

## Build Requirements

- macOS 13.3+ (Ventura or later)
- Apple Silicon (M1/M2/M3/M4)
- Xcode Command Line Tools
- CMake
- Rust 1.82+

The build script will automatically:
1. Clone and build mlx-c
2. Generate Rust bindings using bindgen
3. Link against the compiled library

## Related Crates

| Crate | Description |
|-------|-------------|
| [mlx-rs-burn](https://crates.io/crates/mlx-rs-burn) | Safe Rust bindings (use this!) |
| [mlx-macros-burn](https://crates.io/crates/mlx-macros-burn) | Procedural macros |
| [mlx-internal-macros-burn](https://crates.io/crates/mlx-internal-macros-burn) | Internal macros |
| [burn-mlx](https://crates.io/crates/burn-mlx) | MLX backend for Burn |

## Upstream

Fork of [mlx-sys](https://crates.io/crates/mlx-sys) from [oxideai/mlx-rs](https://github.com/oxideai/mlx-rs).

## License

MIT OR Apache-2.0
