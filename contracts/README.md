# Contract Examples

This folder contains small Soroban contract examples for the playground.

The goal is to give contributors and new users a simple place to find contracts they can read, build, and reuse while testing the project locally.

## What belongs here

Each subfolder in `contracts/` should contain one self-contained example contract.

Examples should stay:

- Small and easy to understand
- Focused on one idea or feature
- Ready to build locally

Current example:

- `hello-world/`: a minimal Soroban contract with a short README

## Recommended structure

Add each new example in its own directory:

```text
contracts/
  example-name/
    README.md
    Cargo.toml
    src/
      lib.rs
```

Use this structure for future examples:

- `README.md`: explains what the example does and how to build or run it
- `Cargo.toml`: Rust package configuration for the contract
- `src/lib.rs`: the contract source code

## Naming and organization

To keep this folder easy to browse:

- Use short, descriptive directory names such as `hello-world` or `counter`
- Keep one example per directory
- Include a README in every example folder
- Avoid mixing unrelated contract ideas in the same example

## Local usage

To try an example locally, move into that contract's directory and build it from there.

Example:

```bash
cd contracts/hello-world
cargo build --target wasm32-unknown-unknown --release
```

After building, the compiled WASM output will be available in Cargo's `target` directory for that contract.

## For contributors

If you add a new contract example:

1. Create a new folder inside `contracts/`
2. Add the contract source files
3. Add a short README that explains the example in beginner-friendly language
4. Keep the example minimal so it is easy for first-time contributors to follow
