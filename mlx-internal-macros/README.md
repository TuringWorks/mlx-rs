# mlx-internal-macros-burn

[![Crates.io](https://img.shields.io/crates/v/mlx-internal-macros-burn.svg)](https://crates.io/crates/mlx-internal-macros-burn)
[![Documentation](https://docs.rs/mlx-internal-macros-burn/badge.svg)](https://docs.rs/mlx-internal-macros-burn)
[![License](https://img.shields.io/badge/license-MIT%2FApache--2.0-blue.svg)](LICENSE)

Internal procedural macros for [mlx-rs-burn](https://crates.io/crates/mlx-rs-burn).

## Overview

This crate provides internal derive macros and procedural macros used by mlx-rs-burn for:
- Automatic trait implementations
- Code generation for MLX operations
- Internal derive macros for array types

## Installation

This crate is automatically included as a dependency of mlx-rs-burn. **You typically don't need to add it directly.**

```toml
[dependencies]
# Just use mlx-rs-burn instead:
mlx-rs-burn = "0.25.4"
```

## Note

This is an internal implementation detail of mlx-rs-burn. The API is not stable and may change without notice. Use [mlx-rs-burn](https://crates.io/crates/mlx-rs-burn) for a stable public API.

## Related Crates

| Crate | Description |
|-------|-------------|
| [mlx-rs-burn](https://crates.io/crates/mlx-rs-burn) | Safe Rust bindings for MLX |
| [mlx-sys-burn](https://crates.io/crates/mlx-sys-burn) | Low-level FFI bindings |
| [mlx-macros-burn](https://crates.io/crates/mlx-macros-burn) | Public procedural macros |
| [burn-mlx](https://crates.io/crates/burn-mlx) | MLX backend for Burn |

## Upstream

Fork of mlx-internal-macros from [oxideai/mlx-rs](https://github.com/oxideai/mlx-rs).

## License

MIT OR Apache-2.0
