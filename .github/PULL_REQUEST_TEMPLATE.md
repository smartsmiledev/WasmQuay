## Motivation

<!-- Why is this change needed? Link the issue if there is one. -->

## What changed

<!-- One behaviour per PR. List the concrete changes. -->

## Checklist

- [ ] `cargo build --offline` passes
- [ ] `cargo test --offline` passes
- [ ] `cargo fmt --check` passes
- [ ] Same input bytes still produce the same manifest (determinism)
- [ ] No new dependencies, no network access
- [ ] For explorer changes: `tsc --noEmit` passes
