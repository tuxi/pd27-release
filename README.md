# PD27 激活补丁包 · 发布与验真页

**作者**：tuxi · [GitHub](https://github.com/tuxi) · [X](https://x.com/thebitcode) · seyooe@gmail.com

> 本页**只用于**：署名、版本说明、**SHA-256 校验值**与**验签方法**。
> 本仓库**不包含**任何二进制、脚本或实现细节。

---

## 适用

- **Parallels Desktop 27.0.3 (58680)**（Build 必须一致）
- macOS + **Apple Silicon（arm64）**

## 产物

- `PD27激活补丁包.pkg`（含欢迎 / 免责声明 / 完成页）
- `PD27激活补丁包.dmg`（一键安装）
- 通过**官方渠道**分发（见下）。

## 校验（拿到文件后请自行核对）

```bash
# 1) 文件完整性
shasum -a 256 -c SHA256SUMS.txt

# 2) 签名 / 公证（应为 accepted / Notarized Developer ID）
/usr/sbin/spctl -a -vv -t install "PD27激活补丁包.pkg"
/usr/sbin/spctl -a -vv -t open --context context:primary-signature "PD27激活补丁包.dmg"
/usr/sbin/pkgutil --check-signature "PD27激活补丁包.pkg"
```

- 预期：`accepted` / `source=Notarized Developer ID` / `origin=Developer ID ... (NKW67GFDHM)`；
- 若**不一致** → 不是官方版本，**可能被篡改，请勿使用**，并从官方渠道重新获取。

## 许可与免责

- **仅限个人自用**；**禁止二次分发与商用**；禁止移除署名（详见 [`LICENSE.txt`](LICENSE.txt)）。
- 本工具按"现状"提供，不提供任何担保；使用风险自负。
- **请支持正版** Parallels Desktop。

## 官方渠道

**仅以作者本人发布的渠道为准**。其它任何来源（网盘、论坛、群组、公众号等）均非官方，可能被篡改或夹带恶意代码。

---

*本页不含任何二进制或脚本；实现细节不在公开范围。*
