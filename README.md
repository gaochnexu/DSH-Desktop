# DeepSeek Harness 桌面版

把 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（`dsh`）的 `dsh web` 服务封装成 Windows 桌面应用（Electron）。

双击图标启动，程序在后台运行 `dsh web --no-open`，主窗口内嵌 Harness 的 Web UI；带启动进度显示、系统托盘菜单、崩溃自动恢复，以及真正退出时对 `dsh` 进程树的清理。

本仓库用于**分发安装包**。

## 下载

| 版本 | 文件 | 大小 | 下载 |
|---|---|---|---|
| v2.4.1 | `DeepSeek Harness Setup 2.4.1.exe` | 106.5 MB | [Releases](https://github.com/gaochnexu/DeepSeekHarness-Desktop/releases/tag/v2.4.1) |

## 安装前须知

**1. 安装包未做代码签名。** Windows SmartScreen 会提示「Windows 已保护你的电脑」，点「更多信息」→「仍要运行」即可。

**2. 安装包不内置 Node 运行时。** 目标机器需要自己具备运行环境（内置 Node 的构建约 133 MB，本包为 106.5 MB）：

| 机器现状 | 你要做的 |
| --- | --- |
| 已有 Node.js + `dsh` | 双击安装包，完事——应用直接使用本机已有的那套 |
| 什么都没有 | 先装 [Node.js](https://nodejs.org)（20.12 以上），再执行 `npm install -g @deepseek-ai/dsh` |

缺环境时应用会把这两步明确写在加载页上，而不是只给一句含糊的报错。

## 校验

```
SHA256  B39AB4F53C2354AA64B655FA91CA65AFDE8576FD9C67C030D70EF9E7F1E26E31
```

PowerShell：

```powershell
Get-FileHash '.\DeepSeek Harness Setup 2.4.1.exe' -Algorithm SHA256
```

## 相关

- DeepSeek Harness 本体：<https://github.com/deepseek-ai/deepseek-harness>（MIT）
- 安装与环境排查：见安装包随附说明
