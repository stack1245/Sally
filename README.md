# Sally Security Shell

[![Release](https://img.shields.io/github/v/release/stack1245/Sally?display_name=tag&sort=semver)](https://github.com/stack1245/Sally/releases/latest)
![Rust](https://img.shields.io/badge/Rust-1.88-000000?logo=rust&logoColor=white)
![Updates](https://img.shields.io/badge/Updates-Ed25519%20signed-5B4BCE)
![Windows](https://img.shields.io/badge/Windows-x86__64-0078D4?logo=windows11&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-x86__64-FCC624?logo=linux&logoColor=111111)
[![License: Proprietary](https://img.shields.io/badge/License-Proprietary-red.svg)](LICENSE)

Sally is a security shell for authorized, workspace-scoped security operations.
It provides one command environment for native tools, managed runtimes,
disposable sandboxes, evidence, and repeatable security workflows. The product
is also described as **Sally Security Shell**, **security shell**, and **Sally
shell**.

This repository is the official public binary distribution channel. It contains
release notes, downloadable packages, checksums, SBOMs, and signed updater
metadata; it does not contain Sally source code or signing private keys. Product
documentation is available at [sally.st4ck.kr](https://sally.st4ck.kr).

## Download

The release badge and the [latest release](https://github.com/stack1245/Sally/releases/latest)
are the authoritative current version.

| Platform | Package |
| --- | --- |
| Windows 10 or later, x86_64 | [`Sally-Windows-x86_64.zip`](https://github.com/stack1245/Sally/releases/latest/download/Sally-Windows-x86_64.zip) |
| Linux, glibc x86_64 | [`Sally-Linux-x86_64.tar.gz`](https://github.com/stack1245/Sally/releases/latest/download/Sally-Linux-x86_64.tar.gz) |
| SHA-256 checksums | [`Sally-SHA256SUMS.txt`](https://github.com/stack1245/Sally/releases/latest/download/Sally-SHA256SUMS.txt) |

Extract the Windows ZIP and run `Sally-Setup.exe`. Windows packages currently
do not carry an Authenticode publisher signature, so Windows may show an
Unknown Publisher warning. Confirm this repository, the exact filename, and
the published SHA-256 before running the installer.

## Release history

Each version keeps its `vX.Y.Z` tag and release notes in the
[release history](https://github.com/stack1245/Sally/releases). Only the
[latest release](https://github.com/stack1245/Sally/releases/latest) retains
downloadable binaries. Older releases remain available as patch-note history
and direct users to the current download.

Signed updater metadata records an internal release revision for downgrade and
replay protection. It is not part of the product version or public GitHub tag.
Sally does not accept unsigned update metadata.

## Verification

Each release includes:

- versionless Windows and Linux packages;
- `Sally-SHA256SUMS.txt` covering every public verification asset;
- CycloneDX SBOMs for both platforms;
- `Sally-Update-Manifest.json` and its exact-byte 64-byte Ed25519 signature;
- immutable release notes identifying product version and release revision.

The stable updater endpoints are:

- `https://sally.st4ck.kr/updates/stable/manifest.json`
- `https://sally.st4ck.kr/updates/stable/manifest.sig`

## License

Sally is proprietary software. Copyright (c) 2026 stack1245. All rights
reserved. See [LICENSE](LICENSE).
