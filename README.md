# ✍️ Shadowing Pro

[![Built with Gemini Pro](https://img.shields.io/badge/AI-Gemini%20Pro-blue?style=flat-square&logo=google-gemini)](https://deepmind.google/technologies/gemini/)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)

**Shadowing Pro** is a lightweight, single-file web application designed for language learners to practice writing and memory through "Shadowing" (Echo Method). It helps you internalize sentence structures by observing, recalling, and rewriting text, with instant AI feedback.

**Shadowing Pro** 是一个轻量级的单文件网页应用，专为语言学习者设计。通过“影子跟读/跟写”法（观察 -> 记忆 -> 复写 -> 对比），帮助您内化语言结构，并提供即时的 AI 纠错反馈。

> **Note:** This project was conceptually designed and entirely coded with the assistance of **Google Gemini Pro**.
>
> **注：** 本项目的设计构思与代码实现均在 **Google Gemini Pro** 的协助下完成。

---

## ✨ Features (功能特性)

* **📝 Dual Modes (双模式):**
    * **Standard Mode:** Blur entire paragraphs to test full recall. (标准模式：全段模糊，点击查看)
    * **Hint Mode:** Show only the first word/characters of each sentence as a cue. (提示模式：首词提示，其余模糊)
* **🤖 Multi-Model AI Support (多模型 AI 支持):**
    * **Google Gemini:** Native support for Gemini 2.5 Flash (Fast & Free tier friendly).
    * **DeepSeek:** Full support for V3 (Chat) and R1 (Reasoner).
    * **OpenAI / Claude / Perplexity:** Compatible with major AI providers.
* **🔍 Smart Diff (智能比对):** Visual highlight of missing words (green) and typos (red) using `diff-match-patch`.
* **⏰ Study Timer (学习计时器):** Supports both Count-up and Pomodoro (Countdown) modes.
* **☕ Donation System (打赏功能):** Integrated WeChat/Alipay QR code modal (customizable via Base64).
* **🎨 Modern UI:** Fully responsive design with **Dark Mode** support, built with Tailwind CSS.
* **🚀 Zero Dependency:** Single HTML file. No build steps, no Node.js required.

---

## 🚀 How to Deploy on GitHub Pages (如何部署)

Since this is a single-file application, deployment is instant.

1.  **Fork** this repository (or create a new one).
2.  Upload the `index.html` file to the root of your repository.
3.  Go to **Settings** -> **Pages**.
4.  Under **Build and deployment**, select **Source** as `Deploy from a branch`.
5.  Select `main` (or `master`) branch and `/ (root)` folder.
6.  Click **Save**. Your site will be live in seconds!

由于这是一个单文件应用，部署非常简单：

1.  **Fork** 本仓库（或新建一个）。
2.  将 `index.html` 文件上传到仓库根目录。
3.  进入 **Settings (设置)** -> **Pages (页面)**。
4.  在 **Build and deployment** 下，选择 **Source** 为 `Deploy from a branch`。
5.  选择 `main` 分支和 `/ (root)` 目录。
6.  点击 **Save**。您的网站将在几秒钟内上线！

---

## ⚙️ Configuration (配置说明)

### 1. AI API Keys
All API keys are stored in your browser's **LocalStorage**. They are never sent to any server other than the official API endpoints (Google, DeepSeek, etc.).
所有 API Key 仅存储在您浏览器的 **本地缓存 (LocalStorage)** 中，除了直接请求官方 API 接口外，绝不会发送到任何第三方服务器。

### 2. Customizing Donation QR Codes (自定义打赏码)
To use your own WeChat/Alipay QR codes:
1.  Convert your QR code images to **Base64** strings (search for "Image to Base64" tools online).
2.  Open `index.html` in a text editor.
3.  Search for the `state` object at the bottom of the script:
    ```javascript
    donation: {
        wechat: "data:image/png;base64,YOUR_WECHAT_BASE64...",
        alipay: "data:image/png;base64,YOUR_ALIPAY_BASE64..."
    }
    ```
4.  Replace the strings with your own Base64 code.
5.  Commit and push the changes.

若要替换为您自己的收款码：
1.  将您的微信/支付宝收款码图片转换为 **Base64** 字符串（可在线搜索“图片转Base64”工具）。
2.  使用文本编辑器打开 `index.html`。
3.  在代码底部找到 `state` 对象配置区域。
4.  替换 `wechat` 和 `alipay` 的字符串为您自己的 Base64 代码。
5.  提交并推送代码。

---

## 🤝 Contributing

This project is open-source. Feel free to open issues or submit pull requests if you have ideas for improvements.

欢迎提交 Issue 或 PR 来改进这个工具。

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
