---
name: Bug report
about: A decoder crash, wrong classification, or bad manifest output
title: ''
labels: ['bug']
assignees: ''
---

**What happened**
A clear description. If the decoder crashed, paste the panic message.

**Input file**
Attach the smallest `.wasm` that reproduces it (or hex-dump the section
headers). Payload bytes can be stripped - headers and import names are enough.

**Command + version**

```text
wasmquay --version
wasmquay inspect <file>
```

**Expected vs actual**

**Environment** (OS, rustc version)
