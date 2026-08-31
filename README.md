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

This repository is the official public binary distribution channel. Each
current release exposes exactly the Windows and Linux install packages, while
release notes remain as version history. It does not contain Sally source code,
signing private keys, updater metadata, checksums, or SBOMs. Product
documentation and the signed update channel are available at
[sally.st4ck.kr](https://sally.st4ck.kr).

## Download

The release badge and the [latest release](https://github.com/stack1245/Sally/releases/latest)
are the authoritative current version.

| Platform | Package |
| --- | --- |
| Windows 10 or later, x86_64 | [`Sally-Windows-x86_64.zip`](https://github.com/stack1245/Sally/releases/latest/download/Sally-Windows-x86_64.zip) |
| Linux, glibc x86_64 | [`Sally-Linux-x86_64.tar.gz`](https://github.com/stack1245/Sally/releases/latest/download/Sally-Linux-x86_64.tar.gz) |

Extract the Windows ZIP and run `Sally-Setup.exe`. Windows packages currently
do not carry an Authenticode publisher signature, so Windows may show an
Unknown Publisher warning. Confirm this repository, the exact filename, and
the SHA-256 recorded in the signed stable update manifest before running the
installer.

## Release history

Each version keeps its `vX.Y.Z` tag and release notes in the
[release history](https://github.com/stack1245/Sally/releases). Only the
[latest release](https://github.com/stack1245/Sally/releases/latest) retains
downloadable binaries. Older releases remain available as patch-note history
and direct users to the current download.

Signed updater metadata uses the same `vX.Y.Z` product release version as the
public GitHub tag to enforce downgrade and replay protection. This is the sole
release identity, and Sally does not accept unsigned update metadata.

## Verification

Each GitHub Release includes exactly:

- versionless Windows and Linux packages;
- immutable release notes identifying the shared `vX.Y.Z` product version.

The trusted release pipeline generates and verifies SHA-256 checksums and
platform CycloneDX SBOMs without attaching them as public Release assets. The
official website serves the exact-byte Ed25519 manifest and signature used by
Sally's updater.

The stable updater endpoints are:

- `https://sally.st4ck.kr/updates/stable/manifest.json`
- `https://sally.st4ck.kr/updates/stable/manifest.sig`

## License

Sally is proprietary software. Copyright (c) 2026 stack1245. All rights
reserved. See [LICENSE](LICENSE).
