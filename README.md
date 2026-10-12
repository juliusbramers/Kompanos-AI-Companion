# Kompanos AI Companion — downloads

Packaged builds of the Kompanos Companion: your own computer as a private AI provider for
Kompanos. This repository holds release downloads only; the source lives in the Kompanos
repository (`companion/`). Each release `vX.Y.Z` matches Kompanos `X.Y.Z`.

| File | For |
|---|---|
| `kompanos-companion-<version>-macos-arm64.tar.gz` | Mac with Apple silicon |
| `kompanos-companion-<version>-macos-x86_64.tar.gz` | Mac with an Intel CPU |
| `kompanos-companion-<version>-windows-x86_64.zip` | Windows (64-bit Intel or AMD) |
| `kompanos-companion-<version>-linux-x86_64.tar.gz` | Linux (64-bit Intel or AMD) |
| `kompanos-companion-<version>-linux-arm64.tar.gz` | Linux (64-bit ARM) |

Check a download against `SHA256SUMS`. Each folder holds the `kompanos-companion` program and
its local AI engine (llama.cpp `llama-server`, in `engine/`). Start with
`kompanos-companion test-hardware`.

**The builds are not signed.** The first start shows a warning:

- macOS: "cannot be opened because Apple cannot check it". Open System Settings → Privacy &
  Security and choose "Open Anyway", or clear the download mark once:
  `xattr -dr com.apple.quarantine kompanos-companion-<version>-macos-<arch>`.
- Windows: SmartScreen "Windows protected your PC". Choose "More info", then "Run anyway".
