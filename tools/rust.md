# Rust

## To start
@tags: rust doc update

```
# Update to the latest version
$ rustup update

# Open documentation
$ rustup doc

# Build a project
$ rustc main.rs
```

## Cargo
@tags: rust cargo

```
# create a project with cargo
$ cargo new <project_name>

# Build a project
$ cargo build

# Build a project for release (with optimizations)
$ cargo build --release

# Build and run a project
$ cargo run

# Check that code compiles
$ cargo check

# Update dependencies' versions
$ cargo update

# Create a new library
$ cargo new --lib <lib_name>

# Run all tests in a project
$ cargo test

# Run all tests in a project and show the printed values for passing tests
$ cargo test -- --show-output

# Run tests containing a substring in their name
$ cargo test <substring>

# Run all the tests from the integration test file tests/abc.rs
$ cargo test --test <abc>

# Rust linting
$cargo clippy --all-features --all-targets -- -D warnings
```
