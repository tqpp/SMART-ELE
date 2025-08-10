# 🏭 MF-StationMonitor

<div align="center">
  <h3>变电站数字孪生大屏监控系统</h3>
  <p>基于 Vue 3 + TypeScript + Three.js 构建的现代化变电站可视化监控平台</p>
  
  <p>
    <a href="https://fengtianxi001.github.io/MF-StationMonitor">🌐 在线演示</a> |
    <a href="#快速开始">🚀 快速开始</a> |
    <a href="#功能特性">✨ 功能特性</a>
  </p>
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/fengtianxi001/MF-StationMonitor/main/screenshots/screenshot01.png" alt="主界面截图" width="800">
</div>

## 📖 项目简介

SMART-ELE 是一个专业的变电站数字孪生大屏监控系统，采用现代化的前端技术栈构建。系统通过 3D 可视化技术，实时展示变电站的运行状态、设备监控数据和告警信息，为电力运维人员提供直观、高效的监控体验。

## ✨ 功能特性

### 🎯 核心功能
- **3D 数字孪生**：基于 Three.js 构建的高精度 3D 变电站模型
- **实时监控**：实时显示设备运行状态和关键参数
- **数据可视化**：使用 ECharts 展示各类监控数据图表
- **智能告警**：设备异常状态实时告警和可视化提示
- **响应式设计**：支持多种屏幕尺寸，自适应布局

### 🛠 技术特性
- **现代化框架**：Vue 3 + Composition API + TypeScript
- **3D 渲染引擎**：Three.js 实现高性能 3D 场景渲染
- **数据可视化**：ECharts 图表库支持多种图表类型
- **动画效果**：GSAP 和 Animate.css 提供流畅动画体验
- **自适应布局**：autofit.js 实现多分辨率屏幕适配
- **代码规范**：ESLint + Prettier + Stylelint 保证代码质量

## 🏗 技术架构

```
MF-StationMonitor/
├── src/
│   ├── components/          # Vue 组件
│   │   ├── Layout*.vue     # 布局组件
│   │   └── WidgetPanel*.vue # 功能面板组件
│   ├── hooks/              # 自定义 Hooks
│   │   ├── useEcharts.ts   # ECharts 图表逻辑
│   │   ├── useStation.ts   # 变电站业务逻辑
│   │   └── useThree.ts     # Three.js 3D 场景逻辑
│   ├── assets/             # 静态资源
│   ├── App.vue             # 根组件
│   └── main.ts             # 应用入口
├── public/                 # 公共资源
├── docs/                   # 构建输出目录
└── screenshots/            # 项目截图
```

## 🚀 快速开始

### 环境要求

- Node.js >= 18.0.0
- npm/yarn/pnpm

### 安装依赖

```bash
# 使用 npm
npm install

# 使用 yarn
yarn install

# 使用 pnpm
pnpm install
```

### 开发环境

```bash
# 启动开发服务器
npm run dev

# 或使用 yarn
yarn dev

# 或使用 pnpm
pnpm dev
```

访问 http://localhost:8090 查看应用

### 生产构建

```bash
# 构建生产版本
npm run build

# 预览构建结果
npm run preview
```

## 📦 主要依赖

### 核心依赖
- **Vue 3** - 渐进式 JavaScript 框架
- **TypeScript** - JavaScript 的超集，提供类型安全
- **Three.js** - 3D 图形库，用于构建 3D 场景
- **ECharts** - 数据可视化图表库
- **GSAP** - 高性能动画库
- **autofit.js** - 屏幕自适应解决方案

### 开发工具
- **Vite** - 现代化构建工具
- **ESLint** - 代码质量检查
- **Prettier** - 代码格式化
- **Stylelint** - CSS 代码规范检查

## 🎨 界面展示

<div align="center">
  <img src="https://raw.githubusercontent.com/fengtianxi001/MF-StationMonitor/main/screenshots/screenshot02.png" alt="详细界面截图" width="800">
</div>

## 📋 可用脚本

```bash
# 开发环境
npm run dev              # 启动开发服务器

# 构建相关
npm run build            # 构建生产版本
npm run build-only       # 仅构建，不进行类型检查
npm run preview          # 预览构建结果

# 代码质量
npm run type-check       # TypeScript 类型检查
npm run lint             # ESLint 代码检查
npm run format           # Prettier 代码格式化
npm run lint:style       # Stylelint 样式检查
```

## 🔧 配置说明

### 屏幕适配配置

项目支持多种屏幕分辨率，在 `src/main.ts` 中配置：

```typescript
const ScreenSize = {
  big: [2560, 1440],      // 大屏幕
  normal: [1920, 1080],   // 标准屏幕
  small: [1280, 720],     // 小屏幕
}['normal']  // 当前使用的分辨率
```

### 开发服务器配置

在 `vite.config.ts` 中可以修改开发服务器设置：

```typescript
server: {
  host: '0.0.0.0',
  port: 8090,
  open: true,
  proxy: {
    '/bridge': {
      target: 'http://your-api-server:port',
      changeOrigin: true,
    },
  },
}
```

## 🤝 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 🙏 致谢

- [Vue.js](https://vuejs.org/) - 渐进式 JavaScript 框架
- [Three.js](https://threejs.org/) - 3D 图形库
- [ECharts](https://echarts.apache.org/) - 数据可视化图表库
- [Vite](https://vitejs.dev/) - 现代化构建工具

---

<div align="center">
  <p>如果这个项目对你有帮助，请给它一个 ⭐️</p>
</div>
