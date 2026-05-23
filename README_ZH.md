# RelayPilot-Plugins

[English](./README.md) | 中文文档

RelayPilot-Plugins 是 RelayPilot 的官方插件仓库。

为 AI 中继平台提供供应商集成和扩展模块，包括余额跟踪、用量统计、成本分析、自动签到、奖励处理、通知推送和其他自动化功能。

## 📋 功能特性

- **供应商集成** - 支持多个 AI 中继平台
- **余额跟踪** - 实时账户余额监控
- **用量统计** - 详细的使用统计和报告
- **成本分析** - 全面的成本分析和拆分
- **自动签到** - 自动化账户签到功能
- **奖励处理** - 自动奖励收集和管理
- **通知推送** - 多渠道通知系统（邮件、Webhook 等）
- **可扩展架构** - 易于开发和集成自定义插件

## 🚀 快速开始

### 前置要求

- Node.js（v14 或更高版本）
- npm 或 yarn 包管理器
- 已安装 RelayPilot 主应用

### 安装

```bash
# 克隆仓库
git clone https://github.com/allenjxd/RelayPilot-Plugins.git

# 进入项目目录
cd RelayPilot-Plugins

# 安装依赖
npm install
# 或
yarn install
```

## 📁 项目结构

```
RelayPilot-Plugins/
├── plugins/                    # 插件模块目录
│   ├── balance-tracker/       # 余额跟踪插件
│   ├── usage-collector/       # 用量统计插件
│   ├── cost-analyzer/         # 成本分析插件
│   ├── auto-checkin/          # 自动签到插件
│   ├── reward-handler/        # 奖励管理插件
│   └── notification-service/  # 通知服务插件
├── docs/                       # 文档
├── examples/                   # 示例插件
├── tests/                      # 测试文件
└── package.json               # 项目依赖
```

## 🔌 可用插件

### 余额跟踪插件
监控和跟踪不同中继供应商的账户余额。

```javascript
import BalanceTracker from './plugins/balance-tracker';

const tracker = new BalanceTracker({
  providers: ['provider1', 'provider2']
});

tracker.fetchBalance().then(balance => {
  console.log(balance);
});
```

### 用量统计插件
从中继账户收集和汇总使用统计。

### 成本分析插件
对中继平台使用进行详细的成本分析。

### 自动签到插件
自动处理各平台的每日账户签到。

### 奖励管理插件
管理和收集来自中继账户的奖励。

### 通知服务插件
通过多个渠道发送通知（邮件、Slack、Webhook 等）。

## 🛠️ 开发自定义插件

### 插件结构

```javascript
// my-plugin/index.js
class MyPlugin {
  constructor(options) {
    this.options = options;
  }

  async execute() {
    // 插件逻辑在这里
  }
}

module.exports = MyPlugin;
```

### 插件配置

```json
{
  "name": "my-plugin",
  "version": "1.0.0",
  "description": "我的自定义插件",
  "main": "index.js",
  "relayPilotPlugin": {
    "type": "provider",
    "hooks": ["onBalanceUpdate", "onUsageCollection"]
  }
}
```

## 📝 配置

在根目录创建 `.env` 文件：

```
RELAY_PILOT_API_URL=http://localhost:3000/api
RELAY_PILOT_API_KEY=your_api_key
NOTIFICATION_WEBHOOK_URL=your_webhook_url
```

## 🤝 参与贡献

欢迎贡献！请遵循以下步骤：

1. Fork 本仓库
2. 创建您的特性分支 (`git checkout -b feature/AmazingPlugin`)
3. 开发和测试您的插件
4. 提交您的更改 (`git commit -m 'Add AmazingPlugin'`)
5. 推送到分支 (`git push origin feature/AmazingPlugin`)
6. 打开 Pull Request

## 📚 文档

有关开发插件的详细文档，请参见 [docs/PLUGIN_DEVELOPMENT.md](./docs/PLUGIN_DEVELOPMENT.md)

## 🐛 bug 报告

发现 bug？请在 [GitHub Issues](https://github.com/allenjxd/RelayPilot-Plugins/issues) 中提交问题。

## 📝 许可证

本项目采用 MIT 许可证 - 详见 LICENSE 文件

## 💬 支持

如需支持和帮助，请：
- 在 [GitHub Issues](https://github.com/allenjxd/RelayPilot-Plugins/issues) 中提问
- 访问 [RelayPilot 主仓库](https://github.com/allenjxd/RelayPilot)

## 📧 联系方式

了解更多信息，请访问 [GitHub 个人资料](https://github.com/allenjxd)

---

**用 ❤️ 创建，作者：allenjxd**
