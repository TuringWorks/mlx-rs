# mlx-macros-burn

[![Crates.io](https://img.shields.io/crates/v/mlx-macros-burn.svg)](https://crates.io/crates/mlx-macros-burn)
[![Documentation](https://docs.rs/mlx-macros-burn/badge.svg)](https://docs.rs/mlx-macros-burn)
[![License](https://img.shields.io/badge/license-MIT%2FApache--2.0-blue.svg)](LICENSE)

Procedural macros for [mlx-rs-burn](https://crates.io/crates/mlx-rs-burn).

## Overview

This crate provides public procedural macros for mlx-rs-burn, including:
- `#[derive(ModuleParameters)]` - Derive macro for neural network module parameters
- Helper macros for defining MLX operations

## Installation

This crate is automatically included as a dependency of mlx-rs-burn. **You typically don't need to add it directly.**

```toml
[dependencies]
# Just use mlx-rs-burn instead:
mlx-rs-burn = "0.25.4"
```

## Available Macros

### `#[derive(ModuleParameters)]`

Automatically implements parameter collection for neural network modules:

```rust
use mlx_macros::ModuleParameters;

#[derive(ModuleParameters)]
struct MyLayer {
    #[param]
    weights: Array,
    #[param]
    bias: Array,
}
```

## Related Crates

| Crate | Description |
|-------|-------------|
| [mlx-rs-burn](https://crates.io/crates/mlx-rs-burn) | Safe Rust bindings for MLX |
| [mlx-sys-burn](https://crates.io/crates/mlx-sys-burn) | Low-level FFI bindings |
| [mlx-internal-macros-burn](https://crates.io/crates/mlx-internal-macros-burn) | Internal macros |
| [burn-mlx](https://crates.io/crates/burn-mlx) | MLX backend for Burn |

## Upstream

Fork of mlx-macros from [oxideai/mlx-rs](https://github.com/oxideai/mlx-rs).

## License

MIT OR Apache-2.0
