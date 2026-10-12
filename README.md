# Coding Bro Lite

Coding Bro Lite 的官方安装包与发布记录。此仓库只用于分发安装包和许可证。

## 下载

[最新正式版 0.1.2](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/tag/v0.1.2)

- [macOS Apple Silicon DMG](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.2/Coding-Bro-Lite_0.1.2_aarch64.dmg)
- [Windows x64 安装程序](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.2/Coding-Bro-Lite_0.1.2_x64-setup.exe)
- [Windows x64 MSI](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.2/Coding-Bro-Lite_0.1.2_x64_en-US.msi)
- [Linux Debian amd64](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.2/Coding-Bro-Lite_0.1.2_amd64.deb)
- [SHA256SUMS](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.2/SHA256SUMS)

## 开始使用

1. 安装 Coding Bro Lite。macOS 打开 DMG，将 App 拖到 Applications。
2. 在「账户 → 创建账户」注册，或登录已有 Coding Bro 账户。昵称至少 2 个字符，密码至少 10 个字符。
3. 在账户页选择金额，通过 Stripe Live 正式支付充值美元余额。支付确认后自动入账。
4. 安装 Codex CLI，选择项目和已开放的模型，点击「启动 Codex」。升级后请从新版 App 重新启动。

Lite 只启动 Codex，可使用后端开放的 GPT 与明确支持 Responses 的兼容模型。当前开放 GPT 5.6 Sol、GPT 5.6 Terra，按原有余额规则计费。Lite 不开放新的订阅购买，原有账户和订阅状态与 Coding Bro 共用。

## 平台验证

macOS Apple Silicon App 和 DMG 已通过 Developer ID 签名、Apple 公证、Gatekeeper，以及真实 Codex CLI 回复和余额扣费验证。Windows 安装包未签名；Windows / Linux 安装包已检查，但桌面运行尚未实机验证。

## 许可证

安装包附带第三方许可证和 NOTICE。本仓库保留 [基础项目许可证](LICENSE)、[Codex 许可证](licenses/codex/LICENSE) 和 [Codex NOTICE](licenses/codex/NOTICE)。
