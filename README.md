# DSH Desktop

基于 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（`dsh`）构建的 Windows 桌面封装。

## ⬇️ 下载

> # 👉 [**点击下载 `DSH-Desktop-Setup-2.4.1.exe`**](https://github.com/gaochnexu/DSH-Desktop/releases/download/v2.4.1/DSH-Desktop-Setup-2.4.1.exe)
>
> **Windows 10 / 11 安装包 · 106.5 MB · v2.4.1**
>
> 查看全部版本 → [Releases](https://github.com/gaochnexu/DSH-Desktop/releases)

---

## 装之前先看两条（30 秒）

**1. 安装时 Windows 可能拦你。** 安装包未做代码签名，SmartScreen 会提示「Windows 已保护你的电脑」——点「更多信息」→「仍要运行」即可。

**2. 本机需要有运行环境。** 安装包不内置 Node 运行时：

| 你的机器 | 你要做的 |
| --- | --- |
| 已有 Node.js + `dsh` | 双击安装包，完事——应用直接使用你已有的那套 |
| 什么都没有 | 先装 [Node.js](https://nodejs.org)（20.12 以上），再执行 `npm install -g @deepseek-ai/dsh` |

缺环境时应用会把这两步明确写在启动页上，不会只给一句含糊报错。

## 这是什么

把 `dsh web` 服务封装成桌面应用：双击图标启动，程序在后台运行 `dsh web --no-open`，窗口内嵌 Harness 的 Web UI；带启动进度显示、系统托盘菜单、崩溃自动恢复，以及真正退出时对 `dsh` 进程树的清理。

安装后在 Windows「应用和功能」里显示为 **DSH Desktop**。

## 文件校验（可选）

```
SHA256  3F1E814AA17E494365848F3BF2421CE4925161F84793C2BB30791CC8445BD3D6
```

PowerShell：

```powershell
Get-FileHash '.\DSH-Desktop-Setup-2.4.1.exe' -Algorithm SHA256
```

## 与 DeepSeek Harness 的关系

本项目是基于 DeepSeek Harness 构建的**第三方封装**，与 DeepSeek 官方没有隶属、合作或背书关系。

DeepSeek Harness 本体：<https://github.com/deepseek-ai/deepseek-harness>（MIT 许可）。
