# 版本历史 / Version history

> 每个版本发布后，其产物的 SHA-256 在此登记，便于"拿来文件 → 核对是不是该版本的官方产物"。
> 旧版本的**文件不会被长期保留**，但**校验值长期有效**（可用于鉴别旧抄袭包）。
> 当前版本：[`SHA256SUMS.txt`](SHA256SUMS.txt) / [`RELEASE.txt`](RELEASE.txt)。
>
> 适用版本始终为 **Parallels Desktop 27.0.3 (58680) · macOS Apple Silicon**。

---

## v1.2.0 — 2026-10-13

说明：**签名策略变更** —— 默认**不再关联 Apple 开发者身份**（`pd27tool` ad-hoc、**PKG/DMG 未签名、不公证**）；产物中移除个人邮箱。
首次打开需 **右键 → 打开**（或 `sudo xattr -dr com.apple.quarantine <文件>`）。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `9cee7f670403c8f340a7036c3990f1e384ab0eaf140c5cca4d51be129b7bae8e` |
| `PD27激活补丁包.dmg` | `34406eb14b3a16608f685fdfb59fefaf72883043cfb7671d9663075057ad996b` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `a5f906be71116d253e8b37772b825ca75a620ccfbb05e0e8d88719a5f8bc923c` |

## v1.1.2 — 2026-10-13

说明：署名改用发布页地址；PKG 三个页面显示**版本 + 构建号**；PKG 内链接改为**可复制文本**；`pd27tool --version` 同步。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `fb0ee5431cb5df48a7ebefb0cae9a43b76097eb93b45798f629cce9183a126ca` |
| `PD27激活补丁包.dmg` | `9a3ca3fcd3a28ceaa0f85d45a08590edc8a940fee68d9ea43b18d3a3e3767e3d` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `a282e1f1c7c27e457f79f9cda8b3e4660019ff968dce66fd4dd4594094320987` |

## v1.1.1 — 2026-10-13

说明：`pd27tool` 新增 **`--version`**（打印 BUILD_ID / 署名 / 补丁条数）。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `2ff0ff668a566e02d50b1fe1959b7d64cb8d718fd092a850d766f577be1e9689` |
| `PD27激活补丁包.dmg` | `27dff137ffa10bbae9822f5d991c7f7ca31422f0c4af637ea53f517f080dc035` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `5f538964eefa93353816cd5d71e8820fbbe61c6ad1d914de1392fde68d9e91ce` |

## v1.1.0 — 2026-10-13

说明：**补丁表编译进 `pd27tool`**（arm64 + 逐字节异或混淆）→ 分发物里无明文偏移/字节。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `cfc279709272b688a09206105e46760b6cf9f04baeae8acab35331db13cdc7c1` |
| `PD27激活补丁包.dmg` | `93fe92f0bdf101c87021ef6a9c977fbc47f7c0278450360275e8237562c7036c` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `b5e859527b4bc10db595da424b12625fcd638b6eff89820247631c1ae5ed32a4` |

## v1.0.0 — 2026-10-12

说明：首个可用版本（激活 + VM 可用 + 不到期 + 屏蔽自动更新 + DMG/PKG 签名公证）。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `ca8fb91034c97e7db4ee4699e086622fd570b863e2cb3502ff317c2f89882e33` |
| `PD27激活补丁包.dmg` | `7c49d522a5b056ca8746001a0c5cad920e5e799d5e1cd5023e85181839888d3c` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `1ed8cc97b9750460e5146e06dc86ab776d1c465aba0aa343843205ff787f7325` |

---

*校验方法见 [README.md](README.md)（`shasum -a 256 -c` / `spctl` / `pkgutil --check-signature`）。*
