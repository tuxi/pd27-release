# 版本历史 / Version history

> 每个版本发布后，其产物的 SHA-256 在此登记，便于"拿来文件 → 核对是不是该版本的官方产物"。
> 旧版本的**文件不会被长期保留**，但**校验值长期有效**（可用于鉴别旧抄袭包）。
> 当前版本：[`SHA256SUMS.txt`](SHA256SUMS.txt) / [`RELEASE.txt`](RELEASE.txt)。
>
> ⚠️ 校验值对应**该版本的发布构建**；**重新构建**得到的产物会因内嵌时间戳不同而**哈希不同**，属正常。
>
> 适用版本始终为 **Parallels Desktop 27.0.3 (58680) · macOS Apple Silicon**。

---

## v1.2.6 — 2026-10-13

说明：外壳安装器的**授权密钥改为 PD 风格** `XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX`（30 位，`A-Z0-9`）；密钥仍即解密口令，错误则拒绝安装。
常规发布产物按需构建，故本版本未登记产物校验值。

## v1.2.5 — 2026-10-13

说明：新增**外壳安装器** `PD27激活安装器.app` —— 双击 → 免责声明 → **输入授权密钥** → 解密内嵌的加密 PKG → 安装（**密钥即解密口令**，错误则拒绝安装）；带接收方水印 + 有效期，ad-hoc 签名、不含源码。交付为 zip + 密钥（分渠道）。
常规发布产物按需构建，故本版本未登记产物校验值。

## v1.2.4 — 2026-10-13

说明：**交付模型调整** —— 评测交付默认改为「**AES-256 加密 zip（内含且仅含 PKG）**」；含源码的加密 DMG 改为可选（`--with-dmg`，**不外发**）。
常规发布产物（DMG/PKG）**按需构建**（`./make_package.sh` / `./make_pkg.sh`），故本版本未随版本登记产物校验值。

## v1.2.3 — 2026-10-13

说明：评测包**内含 PKG 安装器**（欢迎/免责/完成页，带同一水印与有效期）；PKG `postinstall` 也过期即中止安装。**常规发布包内容与 v1.2.0–1.2.2 相同**（未签名 / 未公证）。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `c8d832a6c2ac03ad29c71d5b1d5bd59bb8493f8395050f63ac159f06cc328802` |
| `PD27激活补丁包.dmg` | `0cc61847d0832f90f6a5569a708a3862c4a272b06b05d928a859dccaa5f0952e` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `4d3d25a4d525434e15702323ced7014ffa9f6ef4ee250f212b40f81e3818cd8b` |

## v1.2.2 — 2026-10-13

说明：新增**评测副本有效期**（`PD27_EVAL_DAYS` / `PD27_EVAL_EXPIRE`；过期后安装器 rc=2、工具 rc=10 拒绝运行）。**常规发布包内容与 v1.2.0/1.2.1 相同**（未签名 / 未公证）。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `a492f044d3b9faad07ec17a7374c1151434208a4e5700b17b8882a52ae0adf04` |
| `PD27激活补丁包.dmg` | `f0ceff68082acd5da922a0e3c96261f71f08f4b7de2a9fed8042898f89af40fe` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `3afa995b620cb18eb3426bee01f28d032c639d142d4e295be6c375e7d398b225` |

## v1.2.1 — 2026-10-13

说明：新增**评测交付**能力（`make_eval.sh`：接收方水印 + AES-256 加密 DMG）。**常规发布包内容与 v1.2.0 相同**（未签名 / 未公证）。

| 文件 | SHA-256 |
|------|---------|
| `PD27激活补丁包.pkg` | `a4212777ec1bd43488a51e0ccac2bd4c5b363b84d3efd888e6c203393bdfe1eb` |
| `PD27激活补丁包.dmg` | `455ef1fcfc60d156b7ce47166965a70a5426f7ee34d9b92b0e753df7baa3618d` |
| `PD27-Activation-Pack-27.0.3-58680.tar.gz` | `6da0f8681a7fd7f7aad522f6776045c3225ab6fba71f8fa5143dc10e9abc78fb` |

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
