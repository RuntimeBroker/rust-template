# {{project-name}}

{% if description %}{{description}}{% else %}A Rust project bootstrapped from the rust-template.{% endif %}

## Quick Start

This project was generated from [rust-template](https://github.com/RuntimeBroker/rust-template).

## Included Tooling

| Tool | Purpose |
|------|---------|
| `cargo-nextest` | Fast test runner |
| `cargo-deny` | Dependency license & security audit |
| `typos` | Spell checking |
| `git-cliff` | Changelog generation from conventional commits |
| pre-commit | Pre-commit hooks for code quality |

## Setup

```bash
# Install tools
cargo install cargo-nextest --locked
cargo install cargo-deny --locked
cargo install typos-cli
cargo install git-cliff

# Install pre-commit hooks
pipx install pre-commit
pre-commit install
```

## Commands

```bash
cargo build                 # Build
cargo check --all           # Check (no codegen)
cargo fmt                   # Format
cargo clippy --all-targets --all-features --tests --benches -- -D warnings  # Lint
cargo nextest run --all-features --no-tests warn  # Test
cargo deny check -d         # Security audit
```

## CI

GitHub Actions triggers on push/PR to `master` and version tags (`v*`). Tag pushes auto-generate a changelog and GitHub Release.
