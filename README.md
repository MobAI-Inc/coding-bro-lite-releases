# Coding Bro Lite

Coding Bro Lite 的官方安装包、发布记录和 E2E 操作说明。

## 下载

[最新正式版 0.1.3](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/tag/v0.1.3)

- [macOS Apple Silicon DMG](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.3/Coding-Bro-Lite_0.1.3_aarch64.dmg)
- [Windows x64 安装程序](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.3/Coding-Bro-Lite_0.1.3_x64-setup.exe)
- [Windows x64 MSI](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.3/Coding-Bro-Lite_0.1.3_x64_en-US.msi)
- [Linux Debian amd64](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.3/Coding-Bro-Lite_0.1.3_amd64.deb)
- [SHA256SUMS](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.3/SHA256SUMS)

## 开始使用

1. 安装 Coding Bro Lite。macOS 打开 DMG，将 App 拖到 Applications。
2. 在「账户 → 创建账户」注册，或登录已有 Coding Bro 账户。昵称至少 2 个字符，密码至少 10 个字符。从 Lite 新注册的账户一次性赠送 $10 余额。
3. 在账户页选择金额，通过 Stripe Live 正式支付充值美元余额。支付确认后自动入账，充值 $10 入账 $10。
4. 安装 Codex CLI，选择项目和已开放的模型，点击「启动 Codex」。升级后请从新版 App 重新启动。

Lite 只启动 Codex，可使用后端开放的 GPT 与明确支持 Responses 的兼容模型。所有在 Lite 开放的模型均按官方价格的 20% 扣除余额，包含缓存及长上下文对应费率。Lite 不开放新的订阅购买，原有账户和订阅状态与 Coding Bro 共用。

## 平台说明

macOS Apple Silicon App 和 DMG 使用 Developer ID 签名并经过 Apple 公证。Windows 安装包未签名；Windows / Linux 桌面运行尚未实机验证。

## E2E 操作说明

保留 [E2E 操作步骤和预期结果](docs/e2e.md)，不提供自动化测试脚本。步骤描述不代表已执行；本版本尚未完成实际 Live 银行卡付款到余额入账的全过程。

## 许可证

安装包附带第三方许可证和 NOTICE。本仓库保留 [基础项目许可证](LICENSE)、[Codex 许可证](licenses/codex/LICENSE) 和 [Codex NOTICE](licenses/codex/NOTICE)。
