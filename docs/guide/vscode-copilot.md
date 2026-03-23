# 在 VSCode 中使用 GitHub Copilot 与 Claude Sonnet 4.6 模型

本指南介绍如何在 Visual Studio Code 中登录 GitHub Copilot 并切换到 Claude Sonnet 4.6 模型。

## 前置条件

- 安装 [Visual Studio Code](https://code.visualstudio.com/)
- 拥有有效的 [GitHub 账号](https://github.com/)
- 订阅 [GitHub Copilot](https://github.com/features/copilot)（个人版、商业版或企业版均支持 Claude 模型）

## 安装 GitHub Copilot 扩展

1. 打开 VSCode，点击左侧活动栏的**扩展**图标（快捷键 `Ctrl+Shift+X` / `Cmd+Shift+X`）。
2. 在搜索框中输入 **GitHub Copilot**。
3. 找到 **GitHub Copilot** 扩展，点击**安装**。
4. 同时建议安装 **GitHub Copilot Chat** 扩展，以获得对话式 AI 功能。

## 登录 GitHub Copilot

安装扩展后，VSCode 会提示登录 GitHub 账号：

1. 点击右下角弹出的 **Sign in to GitHub** 提示，或点击状态栏中的 Copilot 图标。
2. 在弹出的对话框中选择**允许**，浏览器将自动打开 GitHub 授权页面。
3. 在浏览器中确认授权后，回到 VSCode，登录即完成。

> **提示：** 若未自动弹出提示，可按下 `Ctrl+Shift+P`（`Cmd+Shift+P`）打开命令面板，输入并执行 `GitHub Copilot: Sign In`。

## 切换到 Claude Sonnet 4.6 模型

GitHub Copilot Chat 支持多种 AI 模型，包括来自 Anthropic 的 Claude 系列模型。

### 方法一：在 Copilot Chat 界面切换

1. 打开 Copilot Chat 面板（点击左侧活动栏的 Copilot Chat 图标，或按 `Ctrl+Alt+I`）。
2. 在对话输入框上方，点击**模型选择下拉菜单**（显示当前模型名称的按钮）。
3. 在模型列表中找到并选择 **Claude Sonnet 4.6**（或 `claude-sonnet-4-6`）。
4. 选择后即可使用该模型进行对话。

### 方法二：通过设置切换默认模型

1. 打开 VSCode 设置（`Ctrl+,` / `Cmd+,`）。
2. 搜索 `github.copilot.chat.defaultModel`。
3. 将值设置为 `claude-sonnet-4-6`。

## 使用 Claude Sonnet 4.6 辅助开发 DataV 项目

切换到 Claude Sonnet 4.6 后，你可以在开发 DataV 组件时充分利用 AI 辅助能力，例如：

- **代码补全**：在编写 Vue 组件时，Copilot 会自动提供代码建议。
- **对话式问答**：在 Copilot Chat 中直接提问，例如：

```
如何在 DataV 的 scrollBoard 组件中动态更新数据？
```

- **代码解释**：选中代码后右键选择 **Copilot > Explain**，让 AI 解释代码逻辑。
- **代码修复**：选中存在问题的代码，使用 `/fix` 命令请求修复建议。

## 常见问题

**Q: 模型列表中没有显示 Claude Sonnet 4.6？**

A: 请确认你的 GitHub Copilot 订阅版本支持 Claude 模型，并将 VSCode 及 GitHub Copilot 扩展更新到最新版本。

**Q: 登录后提示无法访问 Copilot？**

A: 请前往 [GitHub 账号设置](https://github.com/settings/copilot) 确认 Copilot 订阅状态是否正常。

**Q: 如何退出 Copilot 账号？**

A: 打开命令面板（`Ctrl+Shift+P`），执行 `GitHub Copilot: Sign Out` 即可退出。
