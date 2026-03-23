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

安装扩展后需要使用 GitHub 账号授权，以下三种方式均可完成登录。

### 方式一：通过右下角提示登录（推荐）

安装扩展后 VSCode 会在右下角自动弹出登录提示：

1. 点击右下角通知栏中的 **Sign in to GitHub** 按钮。
2. VSCode 弹出对话框询问是否打开浏览器，点击**打开**（Open）。
3. 浏览器跳转到 GitHub 授权页面，确认已登录正确的 GitHub 账号后，点击 **Authorize Visual-Studio-Code** 按钮。
4. 浏览器提示"是否允许打开 VSCode"，点击**允许**。
5. VSCode 自动回到前台，状态栏右下角的 Copilot 图标变为激活状态（不再显示斜线），表示登录成功。

### 方式二：通过命令面板登录

若未弹出提示，或提示已消失，可手动触发：

1. 按下 `Ctrl+Shift+P`（macOS：`Cmd+Shift+P`）打开命令面板。
2. 输入 `GitHub Copilot: Sign In`，回车执行。
3. 后续步骤与方式一的第 2–5 步相同。

### 方式三：通过状态栏图标登录

1. 查看 VSCode 窗口右下角的状态栏，找到 **Copilot 图标**（形似斜线的图标表示未登录）。
2. 点击该图标，在弹出菜单中选择 **Sign in to use GitHub Copilot**。
3. 后续步骤与方式一的第 2–5 步相同。

### 验证登录状态

登录成功后，可通过以下方式确认：

- **状态栏**：右下角的 Copilot 图标显示正常（无斜线）。
- **命令面板**：执行 `GitHub Copilot: Check Status`，提示 `Connected` 表示已连接。
- **账号面板**：点击 VSCode 左下角的账号图标，可以看到已登录的 GitHub 账号。

> **提示：** 如果在中国大陆访问 GitHub 授权页面有困难，建议使用稳定的网络环境完成授权。

## 切换到 Claude Sonnet 4.6 模型

GitHub Copilot Chat 支持多种 AI 模型，包括来自 Anthropic 的 Claude 系列模型。

### 方法一：在 Copilot Chat 界面切换

1. 打开 Copilot Chat 面板（点击左侧活动栏的 Copilot Chat 图标，或按 `Ctrl+Alt+I`）。
2. 在对话输入框上方，点击**模型选择下拉菜单**（显示当前模型名称的按钮）。
3. 在模型列表中找到并选择 **Claude Sonnet 4.6**。
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

**Q: 安装扩展后没有弹出登录提示怎么办？**

A: 可通过以下步骤手动触发：打开命令面板（`Ctrl+Shift+P`），执行 `GitHub Copilot: Sign In`；或点击 VSCode 右下角状态栏中带斜线的 Copilot 图标，选择登录选项。

**Q: 浏览器授权后回到 VSCode 仍未登录成功？**

A: 尝试以下步骤：
1. 关闭并重新打开 VSCode。
2. 确认浏览器弹出的"允许打开 Visual Studio Code"对话框已点击**允许**。
3. 检查是否安装了多个版本的 VSCode（Stable / Insiders），请确保在同一版本中完成授权。

**Q: 登录后提示无法访问 Copilot？**

A: 请前往 [GitHub 账号设置](https://github.com/settings/copilot) 确认 Copilot 订阅状态是否正常。

**Q: 企业账号（GitHub Enterprise）如何登录？**

A: 打开 VSCode 设置，搜索 `github-enterprise.uri`，填入企业 GitHub 实例的地址（如 `https://github.yourcompany.com`），然后通过命令面板执行 `GitHub Enterprise: Sign In` 完成登录。

**Q: 如何退出 Copilot 账号？**

A: 打开命令面板（`Ctrl+Shift+P`），执行 `GitHub Copilot: Sign Out` 即可退出；或点击 VSCode 左下角的账号图标，选择 GitHub 账号旁的**退出登录**。
