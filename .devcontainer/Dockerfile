FROM mcr.microsoft.com/devcontainers/python:3.11

# Install Rust
RUN curl https://sh.rustup.rs -sSf | bash -s -- -y
ENV PATH="/root/.cargo/bin:${PATH}"

# Pre-install maturin (used to build Rust extensions)
RUN pip install maturin

# Install system-level packages needed by maturin and rust
RUN apt-get update && apt-get install -y pkg-config libssl-dev build-essential
