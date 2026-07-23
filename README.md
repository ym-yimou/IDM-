# IDM 激活脚本 📔
一款开源工具，用于激活和重置 [Internet Download Manager](https://www.internetdownloadmanager.com/) 的试用期。

# 功能特性
* 通过注册表密钥锁定方式冻结 IDM 试用期并进行激活
* 即使安装 IDM 更新，激活和试用状态依然保留
* IDM 试用期重置
* 完全开源
* 基于透明的批处理脚本

# 下载 / 如何使用？⬇️
首先，全新安装 [Internet Download Manager](https://www.internetdownloadmanager.com/)。确保之前如果有任何破解/补丁已被移除或卸载。
之后，按照以下步骤进行激活。

# 方法一 – PowerShell（推荐）
* 右键点击 Windows 开始菜单，选择 PowerShell 或终端（不要选 CMD）。
* 复制粘贴以下代码并按回车键：
  ```bash
  irm "https://bit.ly/idm-zh_cn" | iex
  ```
  或
  ```bash
  irm "https://raw.githubusercontent.com/ym-yimou/IDM-/main/IAS.ps1" | iex
  ```
* 你会看到激活选项，按照屏幕上的提示操作即可。
* 就这样，全部完成。

# 截图 📸
![截图1](https://github.com/Astro-Saurav/IDM-Activation-Script/blob/72eae3aa664bb6dd446008dd448fe632f3e7a641/Screenshort/1.png)

![截图2](https://github.com/Astro-Saurav/IDM-Activation-Script/blob/72eae3aa664bb6dd446008dd448fe632f3e7a641/Screenshort/2.png)

# 相关信息 ℹ️
## 冻结试用期 🥶
* IDM 提供 30 天的试用期，你可以使用脚本中的此选项来永久锁定该试用期，这样你就不必再次重置试用期，且试用期永远不会过期。
* 此方法在应用时需要联网。
* IDM 更新可以直接安装，无需再次冻结试用期。

## 激活 ✅
* 本脚本通过注册表锁定方法来激活 Internet Download Manager（IDM）。
* 此方法在激活时需要联网。
* IDM 更新可以直接安装，无需再次激活。
* 激活后，如果在某些情况下 IDM 开始显示激活提示弹窗，只需再次运行激活选项即可，无需使用重置选项。

## 重置 IDM 激活 / 试用期 ®️
* Internet Download Manager 提供 30 天的试用期，你可以随时使用本脚本重置此激活/试用期。
* 如果 IDM 报告虚假序列号或其他类似错误，此选项也可用于恢复状态。

## 系统要求
* 本项目支持 Windows 7/8/8.1/10/11 及其对应服务器版本。
* 通过 PowerShell 运行 IAS 的方法在 Windows 8 及以上版本中受支持。

## 高级信息
* 若要以无人值守模式激活，请使用 `/act` 参数运行脚本。
* 若要以无人值守模式冻结试用期，请使用 `/frz` 参数运行脚本。
* 若要以无人值守模式重置，请使用 `/res` 参数运行脚本。

# 工作原理是什么？
* IDM 将试用和激活相关的数据存储在各个注册表项中。其中一些注册表项会被锁定以防止篡改，并且数据按特定模式存储，用于追踪虚假序列号问题以及剩余试用天数。为了激活它，本脚本通过触发 IDM 中的几次下载来生成这些注册表项，识别出这些注册表项后将其锁定，使 IDM 无法编辑和查看它们。这样一来，IDM 就无法显示"使用虚假序列号激活"的警告。
