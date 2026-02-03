# Situation Monitor 🌍

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fpbeenigg%2Fsituation-monitor&env=VITE_FINNHUB_API_KEY&envDescription=API%20keys%20needed%20for%20the%20application&envLink=https%3A%2F%2Fgithub.com%2Fpbeenigg%2Fsituation-monitor%23environment-variables)

A real-time intelligence and situation awareness dashboard that aggregates news, market data, and geopolitical information from multiple sources. Built with SvelteKit 5 and designed for monitoring global events, financial markets, and emerging narratives.

一个实时情报和态势感知仪表盘，从多个来源聚合新闻、市场数据和地缘政治信息。使用 SvelteKit 5 构建，专为监控全球事件、金融市场和新兴叙事而设计。

## ✨ Features / 功能特点

- **📰 Multi-Source News Aggregation** - 30+ RSS feeds across politics, technology, finance, government, AI, and intelligence sectors
  - **多源新闻聚合** - 涵盖政治、技术、金融、政府、人工智能和情报部门的 30 多个 RSS 源

- **📊 Real-Time Market Data** - Track stocks, commodities, crypto, and sector performance
  - **实时市场数据** - 跟踪股票、大宗商品、加密货币和行业表现

- **🗺️ Interactive Geopolitical Map** - D3.js visualization of global hotspots and conflict zones
  - **交互式地缘政治地图** - 全球热点和冲突区的 D3.js 可视化

- **🔍 Pattern Analysis** - Detect correlations, track narratives, and identify main characters in news
  - **模式分析** - 检测相关性、跟踪叙事并识别新闻中的主要人物

- **🚨 Custom Monitors** - Set up keyword alerts for topics you care about
  - **自定义监控** - 为您关心的主题设置关键词提醒

- **🐋 Whale Tracking** - Monitor large cryptocurrency transactions
  - **巨鲸追踪** - 监控大额加密货币交易

- **🏛️ Government Contracts** - Track federal contract awards
  - **政府合同** - 跟踪联邦合同授予

- **📉 Layoff Monitor** - Stay informed about tech industry layoffs
  - **裁员监控** - 了解科技行业裁员信息

- **🎲 Prediction Markets** - View Polymarket predictions on current events
  - **预测市场** - 查看 Polymarket 对当前事件的预测

- **🖨️ Money Printer** - Federal Reserve indicators and monetary policy tracking
  - **印钞机** - 美联储指标和货币政策跟踪

## 🚀 Tech Stack / 技术栈

- **Frontend**: SvelteKit 2.0 with Svelte 5 reactivity (`$state`, `$derived`, `$effect` runes)
- **Styling**: Tailwind CSS with custom dark theme
- **Type Safety**: TypeScript (strict mode)
- **Visualization**: D3.js for interactive maps
- **Testing**: Vitest (unit) + Playwright (E2E)
- **Deployment**: Static adapter for Vercel/GitHub Pages
- **Data Sources**: GDELT, RSS feeds, CoinGecko, Finnhub, Polymarket

## 📋 Prerequisites / 前置要求

- Node.js 18.x or higher / Node.js 18.x 或更高版本
- npm or pnpm / npm 或 pnpm
- Finnhub API key (free tier available) / Finnhub API 密钥（提供免费套餐）

## 🔧 Local Development / 本地开发

### 1. Clone the repository / 克隆仓库

```bash
git clone https://github.com/pbeenigg/situation-monitor.git
cd situation-monitor
```

### 2. Install dependencies / 安装依赖

```bash
npm install
```

### 3. Configure environment variables / 配置环境变量

Copy the example environment file and add your API keys:

复制示例环境文件并添加您的 API 密钥：

```bash
cp .env.example .env
```

Edit `.env` and add your Finnhub API key:

编辑 `.env` 并添加您的 Finnhub API 密钥：

```env
VITE_FINNHUB_API_KEY=your_api_key_here
```

Get a free API key at: https://finnhub.io/

在此获取免费 API 密钥：https://finnhub.io/

### 4. Start development server / 启动开发服务器

```bash
npm run dev
```

The app will be available at http://localhost:5173

应用程序将在 http://localhost:5173 上可用

### 5. Build for production / 生产构建

```bash
npm run build
npm run preview
```

## 🌐 Deploy to Vercel / 部署到 Vercel

### Option 1: One-Click Deploy / 选项 1：一键部署

Click the button below to deploy directly to Vercel:

点击下方按钮直接部署到 Vercel：

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fpbeenigg%2Fsituation-monitor&env=VITE_FINNHUB_API_KEY&envDescription=API%20keys%20needed%20for%20the%20application&envLink=https%3A%2F%2Fgithub.com%2Fpbeenigg%2Fsituation-monitor%23environment-variables)

You'll be prompted to:
1. Sign in to Vercel (or create an account)
2. Create a Git repository (if deploying from GitHub)
3. Configure environment variables
4. Deploy!

系统将提示您：
1. 登录 Vercel（或创建账户）
2. 创建 Git 仓库（如果从 GitHub 部署）
3. 配置环境变量
4. 部署！

### Option 2: Manual Deployment / 选项 2：手动部署

#### Using Vercel CLI / 使用 Vercel CLI

1. Install Vercel CLI / 安装 Vercel CLI

```bash
npm install -g vercel
```

2. Login to Vercel / 登录 Vercel

```bash
vercel login
```

3. Deploy / 部署

```bash
vercel
```

For production deployment / 生产部署：

```bash
vercel --prod
```

#### Using Vercel Dashboard / 使用 Vercel 仪表板

1. Go to [Vercel Dashboard](https://vercel.com/new)
2. Click "Add New Project" / 点击 "Add New Project"
3. Import your Git repository / 导入您的 Git 仓库
4. Configure project:
   - **Framework Preset**: SvelteKit
   - **Build Command**: `npm run build`
   - **Output Directory**: `build`
5. Add environment variables / 添加环境变量:
   - `VITE_FINNHUB_API_KEY`: Your Finnhub API key / 您的 Finnhub API 密钥
6. Click "Deploy" / 点击 "Deploy"

### Environment Variables / 环境变量

The following environment variable is required for deployment:

部署需要以下环境变量：

| Variable | Description | Required |
|----------|-------------|----------|
| `VITE_FINNHUB_API_KEY` | Finnhub API key for stock market data | Yes / 是 |

You can add these in the Vercel dashboard under **Settings → Environment Variables**.

您可以在 Vercel 仪表板的 **Settings → Environment Variables** 中添加这些变量。

## 📁 Project Structure / 项目结构

```
situation-monitor/
├── src/
│   ├── lib/
│   │   ├── analysis/      # Pattern correlation, narrative tracking
│   │   ├── api/           # Data fetching (GDELT, RSS, markets)
│   │   ├── components/    # Svelte components
│   │   │   ├── layout/    # Header, Dashboard
│   │   │   ├── panels/    # News, Markets, Map, etc.
│   │   │   └── modals/    # Settings, Monitors, Onboarding
│   │   ├── config/        # Feed sources, keywords, analysis patterns
│   │   ├── services/      # CacheManager, CircuitBreaker, ServiceClient
│   │   ├── stores/        # Svelte stores for state management
│   │   └── types/         # TypeScript interfaces
│   ├── routes/            # SvelteKit routes
│   └── app.html           # HTML template
├── static/                # Static assets
├── tests/                 # E2E tests
└── vercel.json            # Vercel configuration
```

## 🧪 Testing / 测试

```bash
# Run unit tests / 运行单元测试
npm run test:unit

# Run E2E tests / 运行 E2E 测试
npm run test:e2e

# Type checking / 类型检查
npm run check

# Linting / 代码检查
npm run lint

# Format code / 格式化代码
npm run format
```

## 🎨 Customization / 自定义

### Adding News Sources / 添加新闻源

Edit `src/lib/config/feeds.ts` to add or remove RSS feeds.

编辑 `src/lib/config/feeds.ts` 以添加或删除 RSS 源。

### Configuring Alerts / 配置提醒

Edit `src/lib/config/keywords.ts` to customize alert keywords and patterns.

编辑 `src/lib/config/keywords.ts` 以自定义提醒关键词和模式。

### Map Hotspots / 地图热点

Edit `src/lib/config/map.ts` to add or modify geopolitical hotspots.

编辑 `src/lib/config/map.ts` 以添加或修改地缘政治热点。

## 🔄 Data Refresh / 数据刷新

The dashboard uses a multi-stage refresh strategy:

仪表板使用多阶段刷新策略：

- **Critical** (immediate): News, markets, alerts
- **Secondary** (2s delay): Crypto, commodities, intel
- **Tertiary** (4s delay): Contracts, whales, layoffs, predictions

Auto-refresh interval can be configured in settings (5-60 minutes).

自动刷新间隔可以在设置中配置（5-60 分钟）。

## 🛡️ Privacy & Security / 隐私与安全

- All data fetching happens client-side
- No user data is collected or stored on servers
- API keys are stored in environment variables
- CORS proxy (Cloudflare Worker) used for RSS feed parsing

所有数据获取都在客户端进行，不会在服务器上收集或存储用户数据。

## 🤝 Contributing / 贡献

Contributions are welcome! Please feel free to submit a Pull Request.

欢迎贡献！请随时提交 Pull Request。

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License / 许可证

This project is open source and available under the [MIT License](LICENSE).

本项目是开源的，采用 [MIT 许可证](LICENSE)。

## 🙏 Acknowledgments / 致谢

- RSS feeds from various news sources
- Market data from Finnhub, CoinGecko
- GDELT Project for global event data
- Polymarket for prediction market data
- D3.js for data visualization

## 📧 Contact / 联系方式

For questions or support, please open an issue on GitHub.

如有问题或需要支持，请在 GitHub 上提出问题。

---

**Live Demo**: [https://hipcityreg-situation-monitor.vercel.app](https://hipcityreg-situation-monitor.vercel.app)

Made with ❤️ using SvelteKit
