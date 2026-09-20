<div align="center">

# Ai-Summary-App

[简体中文](README.md) | **English**

**Make long-form content easier to read and key ideas easier to find.**

An early-stage foundation for an AI-powered summarization app.

![Next.js](https://img.shields.io/badge/Next.js-16-111827?style=flat-square&logo=nextdotjs)
![React](https://img.shields.io/badge/React-19-149ECA?style=flat-square&logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Status](https://img.shields.io/badge/Status-Early_Prototype-6366F1?style=flat-square)

[Overview](#overview) · [Getting Started](#getting-started) · [Roadmap](#roadmap)

</div>

---

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
