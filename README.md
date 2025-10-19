# DX
BNB DEX

Project: A Rust Price Oracle for PancakeSwap (BSC)
We'll build a service that monitors the BNB/USDT liquidity pool on PancakeSwap and provides a price quote API.

Prerequisites
Install Rust: https://www.rust-lang.org/tools/install
Get a BSC RPC URL: You can get a free one from Ankr https://www.ankr.com/ , QuickNode https://www.quiknode.io/ , or run your own node. We'll use a public one for this example, but for production, you'll need a private, reliable one.


Step 1: Set Up the Rust Project

cargo new bsc-dex-backend
cd bsc-dex-backend

Now, add the required dependencies to your Cargo.toml file:

Cargo.html

[package]
name = "bsc-dex-backend"
version = "0.1.0"
edition = "2021"

[dependencies]
# Web framework
axum = "0.7"
# Async runtime
tokio = { version = "1.0", features = ["full"] }
# Ethereum/BSC library
ethers = { version = "2.0", features = ["ws", "rustls"] }
# Serialization
serde = { version = "1.0", features = ["derive"] }
serde_json = "1.0"
# Error handling
anyhow = "1.0"
# For async traits
async-trait = "0.1"

