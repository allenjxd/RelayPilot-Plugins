# RelayPilot-Plugins

[中文文档](./README_ZH.md) | English

RelayPilot-Plugins is the official plugin repository for RelayPilot.

It provides provider integrations and extension modules for AI relay platforms, including balance tracking, usage collection, cost analysis, daily check-ins, reward handling, notifications, and other automation features.

## 📋 Features

- **Provider Integrations** - Support for multiple AI relay platforms
- **Balance Tracking** - Real-time account balance monitoring
- **Usage Collection** - Detailed usage statistics and reporting
- **Cost Analysis** - Comprehensive cost breakdown and analysis
- **Daily Check-ins** - Automated account check-in functionality
- **Reward Handling** - Automatic reward collection and management
- **Notifications** - Multi-channel notification system (Email, Webhook, etc.)
- **Extensible Architecture** - Easy to develop and integrate custom plugins

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager
- RelayPilot main application installed

### Installation

```bash
# Clone the repository
git clone https://github.com/allenjxd/RelayPilot-Plugins.git

# Navigate to the project directory
cd RelayPilot-Plugins

# Install dependencies
npm install
# or
yarn install
```

## 📁 Project Structure

```
RelayPilot-Plugins/
├── plugins/                    # Plugin modules directory
│   ├── balance-tracker/       # Balance tracking plugin
│   ├── usage-collector/       # Usage collection plugin
│   ├── cost-analyzer/         # Cost analysis plugin
│   ├── auto-checkin/          # Daily check-in plugin
│   ├── reward-handler/        # Reward management plugin
│   └── notification-service/  # Notification plugin
├── docs/                       # Documentation
├── examples/                   # Example plugins
├── tests/                      # Test files
└── package.json               # Project dependencies
```

## 🔌 Available Plugins

### Balance Tracker
Monitors and tracks account balances across different relay providers.

```javascript
import BalanceTracker from './plugins/balance-tracker';

const tracker = new BalanceTracker({
  providers: ['provider1', 'provider2']
});

tracker.fetchBalance().then(balance => {
  console.log(balance);
});
```

### Usage Collector
Collects and aggregates usage statistics from relay accounts.

### Cost Analyzer
Performs detailed cost analysis on relay platform usage.

### Auto Check-in
Automatically handles daily account check-ins across platforms.

### Reward Handler
Manages and collects rewards from relay accounts.

### Notification Service
Sends notifications through multiple channels (Email, Slack, Webhook, etc.).

## 🛠️ Developing Custom Plugins

### Plugin Structure

```javascript
// my-plugin/index.js
class MyPlugin {
  constructor(options) {
    this.options = options;
  }

  async execute() {
    // Plugin logic here
  }
}

module.exports = MyPlugin;
```

### Plugin Configuration

```json
{
  "name": "my-plugin",
  "version": "1.0.0",
  "description": "My custom plugin",
  "main": "index.js",
  "relayPilotPlugin": {
    "type": "provider",
    "hooks": ["onBalanceUpdate", "onUsageCollection"]
  }
}
```

## 📝 Configuration

Create a `.env` file in the root directory:

```
RELAY_PILOT_API_URL=http://localhost:3000/api
RELAY_PILOT_API_KEY=your_api_key
NOTIFICATION_WEBHOOK_URL=your_webhook_url
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingPlugin`)
3. Develop and test your plugin
4. Commit your changes (`git commit -m 'Add AmazingPlugin'`)
5. Push to the branch (`git push origin feature/AmazingPlugin`)
6. Open a Pull Request

## 📚 Documentation

For detailed documentation on developing plugins, see [docs/PLUGIN_DEVELOPMENT.md](./docs/PLUGIN_DEVELOPMENT.md)

## 🐛 Bug Reports

Found a bug? Please open an issue in the [GitHub Issues](https://github.com/allenjxd/RelayPilot-Plugins/issues) section.

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 💬 Support

For support and questions, please:
- Open an issue on [GitHub Issues](https://github.com/allenjxd/RelayPilot-Plugins/issues)
- Visit [RelayPilot Main Repository](https://github.com/allenjxd/RelayPilot)

## 📧 Contact

For more information, visit [GitHub Profile](https://github.com/allenjxd)

---

**Made with ❤️ by allenjxd**
