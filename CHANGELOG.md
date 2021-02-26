# Changelog

All notable changes to this project are documented here. The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and this project
adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.5.0] - 2026-08-05

### Added
- Static TypeScript explorer: renders the typed manifest without any runtime.
- Fixture suite for real-world `.wasm` binaries and golden JSON reports.
- GitHub Actions CI: cargo build/test matrix + tsc typecheck for the explorer.

### Changed
- `report` output is now a fully typed JSON manifest (schema-stable keys).
- Capability gate exit codes documented for CI blocking.

## [0.4.0] - 2024-07-30

### Added
- `wit` module: parses WebAssembly interface types into a typed model.
- `compat` checker: flags component/model version mismatches.
- `policy` matcher: wildcard import allowances and deny-by-default rules.

### Changed
- Error taxonomy (`error.rs`) with stable machine-readable codes.

## [0.3.0] - 2022-11-02

### Added
- Capability classification: imports are grouped into host capability
