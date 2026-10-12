# PD27 Activation Pack · Release & Verification

**Author**: tuxi · [GitHub](https://github.com/tuxi/pd27-release) · [X](https://x.com/thebitcode) · seyooe@gmail.com

> This page exists **only** for: attribution, release info, **SHA-256 checksums** and **verification steps**.
> This repository contains **no binaries, no scripts, and no implementation details**.
>
> 📜 **Version history & per-version SHA-256**: [`VERSIONS.md`](VERSIONS.md)
>
> 中文说明见 [README.md](README.md)。

---

## Requirements

- **Parallels Desktop 27.0.3 (58680)** — the build number must match exactly.
- macOS on **Apple Silicon (arm64)**.

## Artifacts

- `PD27激活补丁包.pkg` — installer (Welcome / Disclaimer / Conclusion pages)
- `PD27激活补丁包.dmg` — one-click disk image
- Distributed through the **official channel** only (see below).

## Verify (always check the file you received)

```bash
# 1) Integrity
shasum -a 256 -c SHA256SUMS.txt

# 2) Signature / notarization (expect: accepted / Notarized Developer ID)
/usr/sbin/spctl -a -vv -t install "PD27激活补丁包.pkg"
/usr/sbin/spctl -a -vv -t open --context context:primary-signature "PD27激活补丁包.dmg"
/usr/sbin/pkgutil --check-signature "PD27激活补丁包.pkg"
```

- This pack is **unsigned / not notarized by default** (the author deliberately does **not** associate an Apple Developer identity) →
  `spctl` reports `rejected / Unnotarized` (or `code object is not signed`); **this is expected**.
  On first launch: **right-click → Open**, or run `sudo xattr -dr com.apple.quarantine <file>` first.
- **Authenticity is judged by SHA-256**: it must match [`SHA256SUMS.txt`](SHA256SUMS.txt) (or the matching entry in [`VERSIONS.md`](VERSIONS.md)).
  If it does not match: not an official build — **it may have been tampered with; do not use it**.

## License & Disclaimer

- **Personal use only**; **redistribution and commercial use are prohibited**; you may not remove the attribution (see [`LICENSE.txt`](LICENSE.txt)).
- Provided **"as is"**, without warranty of any kind; use at your own risk.
- Please **support the developers** and buy a Parallels Desktop license if you keep using it.

## Official channel

**Only builds published by the author are official.** Any other source (file hosts, forums, groups, social channels, etc.) is unofficial and may be modified or contain malware.

---

*No binaries or scripts are hosted here; the implementation is not public.*
