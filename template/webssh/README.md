# WebSSH

## Introduction | 简介

**EN**: A simple web application that functions as an SSH client, allowing you to connect to your SSH servers directly from your browser. Built with Python and powered by Tornado, Paramiko, and xterm.js.

**中文**: 一个简单的网页应用，可作为SSH客户端直接通过浏览器连接到SSH服务器。基于Python开发，采用Tornado、Paramiko和xterm.js技术构建。

## Features | 功能特点

**EN**:
* SSH password authentication supported, including empty password.
* SSH public-key authentication supported (DSA, RSA, ECDSA, Ed25519 keys).
* Encrypted keys supported.
* Two-Factor Authentication (time-based one-time password) supported.
* Fullscreen terminal available.
* Resizable terminal window for better user experience.
* Automatic detection of SSH server's default encoding.
* Compatible with modern browsers: Chrome, Firefox, Safari, Edge, and Opera.

**中文**:
* 支持SSH密码认证，包括空密码。
* 支持SSH公钥认证，兼容DSA、RSA、ECDSA、Ed25519等密钥类型。
* 支持加密密钥。
* 支持双因素认证（基于时间的一次性密码）。
* 支持全屏终端模式。
* 终端窗口大小可调整，提升用户体验。
* 自动检测SSH服务器的默认编码。
* 兼容主流浏览器：Chrome、Firefox、Safari、Edge和Opera。

## How it works | 工作原理

**EN**: WebSSH establishes a real-time connection with the browser through WebSocket and forwards requests to the backend powered by Tornado and Paramiko, enabling secure connection and interaction with SSH servers. The process is as follows:

```
+---------+     http     +--------+    ssh    +-----------+
| browser | <==========> | webssh | <=======> | ssh server|
+---------+   websocket  +--------+    ssh    +-----------+
```

This allows users to manage servers conveniently and quickly through a web browser without installing an SSH client locally.

**中文**: WebSSH 通过 WebSocket 与浏览器进行实时交互，并将请求转发给基于 Tornado 与 Paramiko 的后端，实现对 SSH 服务器的安全连接和交互。流程如下所示：

```
+---------+     http     +--------+    ssh    +-----------+
| 浏览器   | <==========> | webssh | <=======> | SSH服务器  |
+---------+   websocket  +--------+    ssh    +-----------+
```

这使得用户无需本地安装 SSH 客户端，即可通过网页浏览器方便快速地完成服务器管理操作。