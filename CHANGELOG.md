# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- `serenie` console command (`serenie --help`, `ingest`, `verify`, `export`)
- `PyYAML` declared as a pinned runtime dependency
- README Support section: the project is free under the MIT license
- `RELEASE_NOTES.md` — public 0.1.0 export notes (clean tree, no private git history, no tip link)

### Changed

- Public license confirmed as MIT, copyright holder `davidlee888686`
- Package metadata uses the GitHub username only (no personal name or email)
- Packaging now installs the `serenie`, `kernel`, and `runtime` packages
- CLI version string set to `0.1.0` to match the package version
- Security reports go through GitHub private security advisories

### Removed

- `LICENSE.CHOOSE.md` (license has been chosen)
- Historical and local-only paths untracked for a future public tree: `serenie_v3_0/`, `.gemini-serenie/`, `.pytest-cache/`, `ops/reports/PHASE_00_REPORT.json`, `ops/cache/metadata.db`, `OWNER_SHIP_CHECKLIST.md`

## [Unreleased] - 2026-11-22

### Removed
- Leftover files from unrelated projects: the engineering program pack folder, a skill-registry manifest, track/OS bootstrap scripts, stale v3.0 release scripts, and speculative JSON spec files under `docs/`. None were used by the CLI or its tests.

### Changed
- Wording cleanup in README, release notes, capability report, owner manifest and package description.

## [0.1.0] - 2026-09-27

### Added
- Owner ship checklist (`OWNER_SHIP_CHECKLIST.md`)
- Package CLI/standard volumes, expanded integration tests (37 passing)

### Fixed
- Empty `authors.email` in `pyproject.toml` so editable install metadata is accepted by setuptools
- Kernel import path so `serenie` package tests collect and pass

### Verified
- Pytest **37/37**
- `serenie_cli.py verify` — ledger hash chain unbroken

## [0.1.0-audit] - 2026-08-04

### Added
- Initial structured release with cleaned, audited repository
- Professional documentation, Dependabot, issue/PR templates, security policy

### Changed
- Updated dependencies: aiohttp 3.14.3, cryptography 50.0.0

### Fixed
- Resolved known vulnerabilities in dependencies

### Removed
- Hermes-agent global dependency (not core to project)
- Temporary and cache directories

---

For updates, see [GitHub Releases](https://github.com/davidlee888686/serenie-cli/releases).
