# Security Policy

## Supported versions

| Version | Supported |
|---------|-----------|
| 0.5.x   | yes       |
| < 0.5   | no        |

## Reporting a vulnerability

WasmQuay is an offline analysis tool, so most web-style vulnerabilities do not
apply - but decoder bugs (panics on malformed input, OOM on crafted section
sizes, incorrect bounds checks in the LEB128 reader) absolutely count.

Please do **not** open a public issue for decoder crashes that could be
triggered by untrusted `.wasm` files. Email the address in the repository
owner profile instead, with:

1. The affected commit (`wasmquay --version` or the git SHA).
2. The smallest `.wasm` input that triggers the behaviour (or a hex dump of
   the relevant bytes - the section headers are usually enough).
3. Expected vs. actual behaviour.

You will get an acknowledgement within a week. Fixes land in the next minor
release and the reporter is credited in the changelog unless they prefer
otherwise.

## Scope

- `wasmquay-core` decoders (leb, wasm, wit) - primary focus.
- `wasmquay-cli` argument handling and file reading.
- The explorer is a static page and never executes analysed input; reports
  about it should be limited to HTML-injection-via-manifest-strings.
