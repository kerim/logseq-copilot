# Logseq Copilot 🚀 - DB Graph Fixed Fork

> **Note**: This is a fork of [EINDEX/logseq-copilot](https://github.com/EINDEX/logseq-copilot) with critical fixes for Logseq DB (database) graph compatibility. See [README-FIXES.md](README-FIXES.md) for detailed information about the fixes.

<p align="center">
  <a href="LICENSE" target="_blank">
    <img alt="GPL-3.0 License" src="https://img.shields.io/github/license/eindex/logseq-copilot.svg?style=flat-square" />
  </a>

  <!-- TypeScript Badge -->
  <img alt="TypeScript" src="https://img.shields.io/badge/-TypeScript-blue?style=flat-square&logo=typescript&logoColor=white" />
</p>

Logseq Copilot is a Chrome extension that allows you to access your Logseq using your browser. Logseq is a privacy-first, open-source platform for knowledge sharing and management. With Logseq Copilot, you can easily retrieve relevant information from your Logseq graph and enrich your online search, reading, and learning experience. 🧠

## ⚠️ What's Different in This Fork

The original extension was experiencing **500 errors** and **failed to display search results** when used with Logseq DB graphs. This fork fixes three critical issues:

1. **Fixed API Method Names** - Updated to use correct Logseq API namespaces (`logseq.App.*`, `logseq.Editor.*`)
2. **Fixed UUID Data Structure** - Corrected mismatch between expected and actual API response format
3. **Fixed getPage Method** - Changed from non-existent `get_page` to `logseq.Editor.getPage`
4. **Added Kagi.com Support** - Improved integration with Kagi search engine with proper sidebar layout

**👉 See [README-FIXES.md](README-FIXES.md) for complete technical details of all fixes.**

## Features

- 🔍 Show Logseq content when you search on popular search engines via your keywords
- **Supported search engines**: Google, Bing, Ecosia, Baidu, Yandex, DuckDuckGo, SearX, **Kagi**, Startpage
- ✅ **Full support for Logseq DB graphs** (fixed in this fork)
- 🔎 **Enhanced Kagi.com integration** with automatic sidebar creation (new in this fork)
- Recall your note on every page
- QuickCapture & advance quick capture, easy and fast making note in Logseq

## Installation

### Prerequisites

1. **Enable Logseq HTTP API**:
   - Open Logseq → Settings → Features
   - Enable "HTTP APIs server"
   - Set an authorization token
   - Note the port (default: 12315)

### Build the Extension

```bash
git clone https://github.com/kerim/logseq-copilot.git
cd logseq-copilot
pnpm install
pnpm run build
```

### Load in Chrome

1. Go to `chrome://extensions`
2. Enable "Developer mode"
3. Click "Load unpacked"
4. Select the `build/chrome-mv3-prod/` directory

### Configure

1. Click the extension icon
2. Enter:
   - **Host**: `localhost`
   - **Port**: `12315`
   - **Token**: Your Logseq API token
3. Click "Test Connection"

## Screenshot

![](docs/screenshots/screenshot.png)

## Original Documentation

[Original Documentation](https://logseq-copilot.eindex.me)

## Contributing

Logseq Copilot is an open-source project and welcomes contributions from anyone who is interested in improving it. If you want to contribute, please follow these steps: 🙌

- Fork this repository and clone it to your local machine. 🍴
- Create a new branch for your feature or bug fix. 🌿
- Make your changes and commit them with a clear and concise message.

## Credits

- [Logseq](https://logseq.com)
- [Original Logseq Copilot by EINDEX](https://github.com/EINDEX/logseq-copilot)
- [chatGPT4Google](https://github.com/wong2/chatgpt-google-extension)

## License

GPLv3

