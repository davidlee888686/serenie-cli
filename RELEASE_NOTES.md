# Serenie 0.1.0 — public MIT release notes

Serenie is a free, local command-line tool for deterministic engineering records. You give it a source or specification file; it checks and canonicalizes the content, assigns a SHA-256 content-addressed identity, and appends a hash-chained evidence record. You can later verify that the ledger is unbroken and export it as JSON.

This is a developer tool, not a chat assistant, and it is not Serien (a separate recovery toolkit). Aria remains the main product.

## What is in this tree

- MIT license, copyright holder `davidlee888686` (GitHub username only)
- Installable package `serenie==0.1.0` with the `serenie` console command
- Kernel, runtime helpers, tests, docs, and CI workflow
- No tip or sponsor link

## Quick start

```bash
python -m venv .venv
# Activate the environment, then:
python -m pip install -e ".[dev]"
python -m pytest -q
serenie --help
serenie verify
```

The source-tree wrapper `python serenie_cli.py ...` works the same way.

## Publishing notes

The public repository is [`davidlee888686/serenie-cli`](https://github.com/davidlee888686/serenie-cli). Clone, badge, and package URLs in this tree point there.

The existing private repository `davidlee888686/Serenie` stays private. Do not make it public, and do not copy or push its `.git` history. That history is about 1.27 GB and still contains large historical blobs and personal data from earlier commits.

This tree is a clean export with a fresh git history only. No tip or sponsor link. No PyPI upload in this release.
