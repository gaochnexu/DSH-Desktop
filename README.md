# DeepSeek Harness 桌面版

## ⬇️ 下载

> # 👉 [**点击下载 `DeepSeek.Harness.Setup.2.4.1.exe`**](https://github.com/gaochnexu/DeepSeekHarness-Desktop/releases/download/v2.4.1/DeepSeek.Harness.Setup.2.4.1.exe)
>
> **Windows 10 / 11 安装包 · 106.5 MB · v2.4.1**
>
> 查看全部版本 → [Releases](https://github.com/gaochnexu/DeepSeekHarness-Desktop/releases)

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

把 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（`dsh`）的 `dsh web` 服务封装成 Windows 桌面应用（Electron）。

双击图标启动，程序在后台运行 `dsh web --no-open`，主窗口内嵌 Harness 的 Web UI；带启动进度显示、系统托盘菜单、崩溃自动恢复，以及真正退出时对 `dsh` 进程树的清理。

## 文件校验（可选）

```
SHA256  B39AB4F53C2354AA64B655FA91CA65AFDE8576FD9C67C030D70EF9E7F1E26E31
```

PowerShell：

```powershell
Get-FileHash '.\DeepSeek.Harness.Setup.2.4.1.exe' -Algorithm SHA256
```

> 打包产物的原始文件名是 `DeepSeek Harness Setup 2.4.1.exe`（带空格）。上传到 GitHub Release 后空格被自动改写成点，下载时以 Release 上的实际文件名为准。
