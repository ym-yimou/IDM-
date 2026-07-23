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
