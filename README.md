# Serenie

Serenie is a local, deterministic engineering tool. You give it a source or specification file, it checks and canonicalizes the content, assigns a content-addressed identity, and appends a record to a hash-chained evidence ledger. You can verify that ledger later and export it as JSON.

It is a command-line developer tool, not a chat assistant. It is also not **Serien**, the separate recovery toolkit.

[![CI](https://github.com/davidlee888686/serenie-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/davidlee888686/serenie-cli/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

## What it does

- **Ingest** a file into the ledger (`ingest`)
- Reject incomplete placeholder code (`TODO`, `FIXME`, `XXX`)
- Canonicalize input and identify it with SHA-256 content addressing
- Record evidence in a hash-chained ledger
- **Verify** that the ledger chain is unbroken (`verify`)
- **Export** the chain as JSON (`export`)

## Requirements

- Python 3.9 or later (3.11 recommended; CI uses 3.11)
- Git
- A virtual environment (do not install into the system Python)

## Install

```bash
git clone https://github.com/davidlee888686/serenie-cli.git
cd Serenie
python -m venv .venv
```

Activate the environment (`source .venv/bin/activate` on macOS/Linux, `.venv\Scripts\activate` on Windows), then:

```bash
python -m pip install -e ".[dev]"
python -m pytest -q
serenie --help
serenie verify
```

## Quickstart

```bash
serenie --help
serenie ingest --file path/to/source.py
serenie verify
serenie export
```

The source-tree script `python serenie_cli.py ...` still works the same way.

Higher-level notes: [docs/README.md](docs/README.md). Capability measurements: [CAPABILITY_REPORT.md](CAPABILITY_REPORT.md).

## Project layout

| Path | Role |
|---|---|
| `serenie/` | Installable package: kernel, public CLI, and package tests |
| `kernel/` | Kernel modules also imported as `kernel` |
| `runtime/` | Runtime helpers used by the CLI (storage, validation, discovery) |
| `serenie_cli.py` | Source-tree wrapper around the `serenie` command |
| `tests/` | Integration tests |
| `docs/` | Documentation |
| `ops/` | Local CI runner and operational scripts |

## Support

Serenie is free to use under the MIT license. Questions and bug reports are welcome as GitHub issues on this repository.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md). Security reports: [SECURITY.md](SECURITY.md).

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

MIT — see [LICENSE](LICENSE). Copyright (c) 2026 davidlee888686.

## Maintainers

[davidlee888686](https://github.com/davidlee888686)

## Contact, support and custom work

- **Bugs and questions:** open an issue at https://github.com/davidlee888686/serenie-cli/issues
- **Ideas, real-world use cases and collaboration:** start a thread in Discussions at https://github.com/davidlee888686/serenie-cli/discussions
- **Custom builds, business applications or partnerships:** open an issue titled `Work with me` and I will reply there.
- More projects: https://github.com/davidlee888686

Serenie is a free starting point. More tools are on the way.

