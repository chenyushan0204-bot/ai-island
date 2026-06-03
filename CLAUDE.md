# AI Island 项目指南

## 项目概述
AI Island 是一个 Electron 桌面应用，在 Mac 状态栏显示桌宠，实时感知 Claude Code / Codex 等 AI 编码助手的运行状态，通过动画、声音、气泡反馈。

## 技术栈
- Electron + JavaScript (CommonJS)
- 无 TypeScript，无构建工具，直接运行 .js 文件
- 打包: electron-builder
- 更新: electron-updater + GitHub Releases

## 项目结构
```
src/              — 主进程 + 渲染进程代码
  main.js         — Electron 入口
  menu.js         — 状态栏托盘菜单
  settings-*.js   — 设置面板（多 Tab）
  i18n.js         — 菜单/气泡多语言
  settings-i18n.js — 设置面板多语言
  prefs.js        — 偏好设置存储
  updater.js      — 更新检查
themes/           — 主题（默认: 小克）
assets/           — SVG 素材、音效、图标
hooks/            — 各 AI Agent 的 hook 脚本
```

## 启动命令
```bash
npm install
npm start          # 开发运行
npm run build:mac  # 打包 Mac DMG（x64 + arm64）
```

## GitHub 仓库
chenyushan0204-bot/ai-island
SSH: git@github.com:chenyushan0204-bot/ai-island.git
