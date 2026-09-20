<div align="center">

# Ai-Summary-App

**让长内容更易读，让关键信息更清晰。**

An early-stage foundation for an AI-powered summarization app.

![Next.js](https://img.shields.io/badge/Next.js-16-111827?style=flat-square&logo=nextdotjs)
![React](https://img.shields.io/badge/React-19-149ECA?style=flat-square&logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Status](https://img.shields.io/badge/Status-Early_Prototype-6366F1?style=flat-square)



</div>

---

点击下方语言标题展开或收起内容，无需离开当前页面。

Click a language heading below to expand or collapse its content on this page.

<details open>
<summary><strong>简体中文</strong> · 点击展开 / 收起</summary>

[项目介绍](#项目介绍) · [本地运行](#本地运行) · [开发路线](#开发路线)

## 项目介绍

Ai-Summary-App 探索一个简单的阅读流程：输入内容，提炼要点，再把摘要带回日常学习和工作。项目采用 Next.js 全栈结构，将页面交互与 API 放在同一个应用中，为后续接入大模型摘要能力打基础。

> **当前阶段：基础原型。** 仓库已实现首页和前后端连通性检查，尚未接入大模型，也尚未实现文本摘要或文档上传。下面的开发路线代表后续方向。

## 当前实现

- **应用首页**：React 客户端页面，展示应用名称和后端连接状态。
- **一键健康检查**：点击 `Check backend` 调用 `/api/health`，在页面显示结果。
- **同源 API 路由**：使用 Next.js App Router 的 Route Handler 返回 JSON。
- **开发基础**：TypeScript、Tailwind CSS 4 和 ESLint 配置。

## 本地运行

准备 Node.js 22 LTS 和 npm，在终端执行：

```bash
git clone https://github.com/langezhang/Ai-Summary-App.git
cd Ai-Summary-App/my-app
npm ci
npm run dev
```

打开 [http://localhost:3000](http://localhost:3000)，点击 **Check backend**。成功时，页面显示：

```text
Backend says: Next.js backend is running
```

直接访问 `/api/health`，接口返回：

```json
{
  "ok": true,
  "message": "Next.js backend is running"
}
```

当前原型不需要 API Key 或环境变量。仓库根目录的 `.env.example` 尚不是可用的环境配置模板，无需复制。

## 项目结构

```text
Ai-Summary-App/
├── README.md
├── README.en.md               # English documentation
└── my-app/                    # 应用目录，npm 命令在这里执行
    ├── app/
    │   ├── page.tsx           # 首页与健康检查交互
    │   ├── layout.tsx         # 根布局
    │   ├── globals.css        # 全局样式
    │   └── api/health/route.ts # 健康检查接口
    ├── public/                # 静态资源
    └── package.json
```

## 开发命令

在 `my-app/` 目录执行：

```bash
npm run dev    # 本地开发
npm run lint   # ESLint 检查
npm run build  # 生产构建
npm run start  # 启动已构建的应用
```

## 开发路线

- [ ] 初始化 Next.js + TypeScript 应用
- [ ] 实现首页和后端健康检查
- [ ] 增加文本输入与摘要结果展示
- [ ] 在服务端接入大模型 API
- [ ] 支持摘要长度、语言与输出格式选择
- [ ] 完善加载状态、失败提示和自动化测试

## 交流与反馈

欢迎通过 [Issues](https://github.com/langezhang/Ai-Summary-App/issues) 提出建议，或通过 Pull Request 参与改进。反馈问题时，请说明复现步骤与预期结果。

</details>

<details>
<summary><strong>English</strong> · Click to expand / collapse</summary>

[Overview](#overview) · [Getting Started](#getting-started) · [Roadmap](#roadmap)

## Overview

Ai-Summary-App explores a simple reading workflow: provide content, extract the main ideas, and use the summary in everyday learning and work. Built as a full-stack Next.js application, it keeps the user interface and API in one project, laying the groundwork for future AI summarization features.

> **Current stage: early prototype.** The repository includes a landing page and a frontend-to-backend connectivity check. It does not yet integrate a language model, generate summaries, or support document uploads. The roadmap below describes planned work.

## What's Implemented

- **Landing page**: a React client component displaying the app name and backend connection status.
- **One-click health check**: the `Check backend` button calls `/api/health` and displays the result.
- **Same-origin API route**: a Next.js App Router Route Handler returns a JSON response.
- **Development foundation**: TypeScript, Tailwind CSS 4, and ESLint configuration.

## Getting Started

Install Node.js 22 LTS and npm, then run:

```bash
git clone https://github.com/langezhang/Ai-Summary-App.git
cd Ai-Summary-App/my-app
npm ci
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) and click **Check backend**. A successful check displays:

```text
Backend says: Next.js backend is running
```

Visiting `/api/health` directly returns:

```json
{
  "ok": true,
  "message": "Next.js backend is running"
}
```

The current prototype does not require an API key or environment variables. The repository-root `.env.example` is not yet a usable environment configuration template and does not need to be copied.

## Project Structure

```text
Ai-Summary-App/
├── README.md                  # Chinese documentation
├── README.en.md               # English documentation
└── my-app/                    # Application directory; run npm commands here
    ├── app/
    │   ├── page.tsx           # Landing page and health-check interaction
    │   ├── layout.tsx         # Root layout
    │   ├── globals.css        # Global styles
    │   └── api/health/route.ts # Health-check endpoint
    ├── public/                # Static assets
    └── package.json
```

## Development Commands

Run these commands from `my-app/`:

```bash
npm run dev    # Start the development server
npm run lint   # Run ESLint
npm run build  # Create a production build
npm run start  # Serve the production build
```

## Roadmap

- [ ] Initialize a Next.js + TypeScript application
- [ ] Add a landing page and backend health check
- [ ] Add text input and summary results
- [ ] Integrate a language model API on the server
- [ ] Support summary length, language, and output-format options
- [ ] Improve loading states, error messages, and automated tests

## Feedback & Contributions

Suggestions are welcome through [Issues](https://github.com/langezhang/Ai-Summary-App/issues), and improvements through pull requests. When reporting a problem, include steps to reproduce it and the expected behavior.

</details>
