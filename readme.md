# 📡 FreeAPI Radar — 免费 API 与 AI 大模型额度雷达

一个**纯前端、无后端**的实时情报站：自动从 GitHub 与公开清单抓取免费 API、对应 curl 示例，并汇总各厂商免费 AI 大模型额度。

## ✨ 功能

| 模块 | 说明 |
|---|---|
| 🌐 免费 API 总库 | 实时抓取 [public-apis/public-apis](https://github.com/public-apis/public-apis)（1400+ 免费 API），按分类/鉴权方式筛选，自动生成对应 curl，一键复制 |
| 🤖 免费 AI 大模型额度 | 内置人工核验的厂商情报（Google Gemini / Groq / OpenRouter / GitHub Models / Cloudflare / Mistral / Cerebras / SambaNova / NVIDIA / Cohere / 智谱 / 百炼 / 千帆 / 硅基流动 / Kimi / DeepSeek …），附领取链接与 curl；并实时抓取社区维护的 [free-llm-api-resources](https://github.com/cheahjs/free-llm-api-resources) 清单 |
| 🐙 GitHub 实时抓取 | 通过 GitHub Search API 实时抓取「最近更新」与「高星」的免费 API / 免费 AI 相关仓库 |
| ⏱ 定时自动重抓 | 可选 5/10/30/60 分钟自动刷新，带倒计时；断网或限流时自动回退内置数据 |

## 🚀 使用

- **在线访问**：GitHub Pages 地址（仓库 → Settings → Pages 开启后生效）
- **本地运行**：直接双击 `index.html` 即可，无需任何服务器

## 🔧 技术说明

- 单文件 `index.html`（内联 CSS/JS），零依赖、零构建，可直接托管在 GitHub Pages
- 数据全部在浏览器端实时抓取：
  - `raw.githubusercontent.com`（public-apis 清单、free-llm 清单）
  - `api.github.com` Search API（实时仓库情报；未登录限流 60 次/小时，页面会自动提示并回退）
- curl 中的 `YOUR_API_KEY` / `$XXX_API_KEY` 请替换为在各官网领取的真实密钥
- 免费额度信息以各厂商官网实时为准，本站情报定期复查更新
