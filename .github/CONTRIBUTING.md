# Contributing to WasmQuay

Thanks for your interest in improving WasmQuay! This project is a 100% offline
toolkit - please keep it that way.

## Ground rules

- **Zero runtime dependencies.** `wasmquay-core` uses only `std`. The explorer
  is `tsc`-only, no npm packages. If your change needs a dependency, it needs a
  very good reason (there has not been one yet).
- **No network access, ever.** All parsing and classification happens on bytes
  the user already has on disk.
- **Deterministic output.** Same input bytes must always produce the same
  manifest, byte for byte.

## Workflow

1. Fork / branch from `main` (`feature/<topic>` or `fix/<topic>`).
2. Make the change. Keep PRs small and focused - one behaviour per PR.
3. Check locally:
   ```bash
   cargo build --offline
   cargo test --offline
   ```
   For explorer changes: `cd explorer && tsc --noEmit`.
4. Open the PR with a short description of *why*, not just *what*.

## Adding fixtures

Real-world `.wasm` samples are the most valuable contributions. Drop the file
in `fixtures/` (keep it under 64 KB, strip symbols if possible) and regenerate
the golden JSON with `make fixtures`.

## Reporting issues

Use the bug report template. Always attach the **capability classification**
output (it is safe - it contains only section/import names, never payload
bytes) and the exact `wasmquay --version`.

## Code style

- `rustfmt` defaults; `cargo fmt --check` must pass.
- Public items need doc comments; stable JSON keys are part of the API and are
  never renamed without a major version bump.
