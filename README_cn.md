# zmodem-ts-demo

[zmodem-ts](https://github.com/zxdong262/zmodem-ts) 演示项目 - 一个用于 Web 终端的 Zmodem 文件传输协议的 TypeScript 实现。

这个基于 Web 的终端应用程序通过 WebSocket 连接到 SSH 服务器，并演示了使用 zmodem-ts 进行 Zmodem 文件传输。

[English](README.md) | [中文](README_cn.md)

## 关于 zmodem-ts

[zmodem-ts](https://github.com/zxdong262/zmodem-ts) 是一个 TypeScript 库，为现代 Web 应用程序实现了 Zmodem 文件传输协议。它实现了 Web 终端与远程服务器之间的可靠文件传输。

## 功能特性

- 使用 xterm.js 的基于 Web 的终端
- 到后端的 WebSocket 连接
- 到远程服务器的 SSH 连接
- 使用 zmodem-ts 的 Zmodem 文件传输支持

## 安装设置

1. 安装依赖：

   ```bash
   npm install
   ```

2. 启动 Docker 测试服务器：

   ```bash
   cd src/dockers
   docker build -t zmodem-test-server .
   docker run -d -p 23355:22 --name zmodem-test zmodem-test-server
   ```

3. 启动后端：

   ```bash
   npm run backend
   ```

4. 启动前端：

   ```bash
   npm run dev
   ```

5. 在浏览器中打开 `http://localhost:3001`。

## 项目结构

- `src/client`：前端 React TypeScript 代码
- `src/server`：后端 TypeScript 代码
- `build/`：构建配置
- `src/dockers/`：测试服务器的 Docker 设置

## 技术栈

- 前端：React, Vite, TypeScript, xterm.js, zmodem-ts
- 后端：Express, express-ws, ssh2
- 构建：Vite
- 测试服务器：带有 OpenSSH 的 Docker

## 使用 zmodem-ts

这个演示展示了如何在 Web 终端应用程序中集成 zmodem-ts。关键实现文件：

- `src/client/zmodem/send.ts` - 通过 Zmodem 发送文件
- `src/client/zmodem/offer.ts` - 通过 Zmodem 接收文件
- `src/client/zmodem/addon.ts` - xterm.js 插件集成

有关使用 zmodem-ts 的更多详细信息，请访问 [zmodem-ts 仓库](https://github.com/zxdong262/zmodem-ts)。