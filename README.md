# Coding Bro Lite

Coding Bro Lite 的官方安装包、发布记录和 E2E 操作说明。

## 下载

[最新正式版](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/latest)

0.1.5 安装包：

- [macOS Apple Silicon DMG](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.5/Coding-Bro-Lite_0.1.5_aarch64.dmg)
- [Windows x64 安装程序](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.5/Coding-Bro-Lite_0.1.5_x64-setup.exe)
- [Windows x64 MSI](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.5/Coding-Bro-Lite_0.1.5_x64_en-US.msi)
- [Linux Debian amd64](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.5/Coding-Bro-Lite_0.1.5_amd64.deb)
- [SHA256SUMS](https://github.com/MobAI-Inc/coding-bro-lite-releases/releases/download/v0.1.5/SHA256SUMS)

## 开始使用

1. 安装 Coding Bro Lite。macOS 打开 DMG，将 App 拖到 Applications。
2. 在「账户 → 创建账户」注册，或登录已有 Coding Bro 账户。昵称 2–40 个字符，密码 10–128 个字符。从 Lite 新注册的账户一次性赠送 $10 余额；已有账户登录、刷新或重复注册不会再次赠送。
3. 在账户页选择金额，通过 Stripe Live 正式 Checkout 充值美元余额。支持银联等银行卡，具体以发卡行和支付页为准；银联使用普通银行卡表单，不是单独的支付方式按钮。支付确认后自动入账，充值 $10 入账 $10。
4. 选择模型和启动方式：
   - **终端 · Codex CLI**：安装官方 CLI，选择项目目录，点击「启动 Codex 终端」。
   - **官方 Codex / ChatGPT App**：安装受支持的官方 App，点击「打开官方 App · 使用 Lite 配置」。可以不选项目目录；需要项目时也可先指定目录。

官方 App 入口使用独立的配置与用户数据目录，加载所选模型、Lite provider 和账户凭据助手，不覆盖个人 App 配置或复制个人 ChatGPT 登录凭据。退出 Lite、切换账户或重新登录后，请从 Lite 重新启动；正常会话刷新保留原会话绑定。官方 App 若要求额外登录，按其版本或组织政策提示完成。打开窗口不代表实际模型回复或计费已验证。

## 模型和优惠

目前服务端目录开放以下五个同名 GPT 候选型号；以登录后的实时目录为准。目录登记代表允许选择，不证明实际上游供给或请求成功，不能把未供给型号替换成另一个模型：

| 型号          | 精确模型 ID     |
| ------------- | --------------- |
| GPT-5.5       | `gpt-5.5`       |
| GPT-5.6 Sol   | `gpt-5.6-sol`   |
| GPT-5.6 Terra | `gpt-5.6-terra` |
| GPT-6 Astra   | `gpt-6-astra`   |
| GPT-6.1 Sol   | `gpt-6.1-sol`   |

**GPT-5.6 Luna（`gpt-5.6-luna`）和 GPT-5.5 Pro（`gpt-5.5-pro`）明确不提供**：不显示可用报价、不允许启动，后台应拒绝这两个型号的请求。旧页面或已打开的官方 App 保留历史目录时，请刷新 Lite 并从 Lite 重新启动；不能将旧目录视为已恢复供给。

上述 GPT 使用 **OpenAI 官网 Standard 标准处理价格的 20%** 计费，按服务端固定的官方价格快照计算，包含该型号明确列出的缓存读取、缓存写入及长上下文费率；不会采用 Batch / Flex / Fast 价格或猜测其它型号的费率。应用展示实际服务端报价，计费政策为 `codex-lite-official-v1`。整笔费用只在最后向上取整到 microUSD；充值金额不打折，仍是 1 USD 支付 = 1 USD 入账。

当前目录开放的五个候选 GPT 在 Lite 使用 Standard 默认档位；显式选择其它处理档位会提示不支持，并在上游调用前拒绝。

0.1.5 区分缓存读取和缓存写入报价：服务端提供短 / 长上下文写缓存价时，应用分别显示，不向未提供该字段的型号增加费用项。有写缓存报价的型号按总输入扣除缓存读、写 token 后计算普通输入，三类输入各计一次费用；缓存费同样按对应官方费率的 20% 扣除。

Lite 只接 Codex，可选择服务端开放的 GPT 与明确支持 OpenAI Responses、具有官方价格依据的兼容模型；实际供给仍需真实请求确认。Lite 不开放新的订阅购买，原有账户和订阅状态与 Coding Bro 共用。

## 平台说明

0.1.5 macOS Apple Silicon App 和 DMG 已完成 Developer ID 签名、Apple 公证、stapling 和安装包验证。三个平台安装包均构建成功，下载后 SHA256SUMS 校验通过。Windows 安装包未签名；Windows / Linux 桌面运行尚未实机验证。

官方 App 入口在 macOS 使用官方 App 的独立实例机制；Windows 仅检测受支持的直接安装布局，未识别的商店安装会提示使用终端。Linux 使用终端入口。本版本未执行官方 App 启动、实际模型回复或 Live 银联付款到余额入账的人工 E2E。

## E2E 操作说明

保留 [E2E 操作步骤和预期结果](docs/e2e.md)，不提供自动化测试脚本。文档包含客户端与后台的人工步骤：注册赠金、双启动入口、候选模型选择、不可用型号的拒绝、余额变化、缓存及长上下文计费，以及 Live 银行卡和银联付款。步骤描述不代表已执行。

## 许可证

安装包附带第三方许可证和 NOTICE。本仓库保留 [基础项目许可证](LICENSE)、[Codex 许可证](licenses/codex/LICENSE) 和 [Codex NOTICE](licenses/codex/NOTICE)。
