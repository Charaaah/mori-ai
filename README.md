# Mori · AI 创作空间 UI

薄荷绿风格的中文 AI 网页界面，包含自由对话和图片创作两种模式。纯前端 UI 预览：聊天使用本地示例，图片展示所选尺寸的预览画布，不调用真实模型，也不需要任何密钥。

## 文件夹内容

- `index.html`：发布版网页。单个文件包含全部样式和脚本，直接放到静态托管服务即可。
- `源文件/`：可编辑源码。`index.html` 结构、`styles.css` 样式、`app.js` 界面逻辑、`demo.js` 示例内容、`server.cjs` 本机预览服务器、`package.json` 脚本。

## 发布给别人访问

任选一种，都是免费的静态托管：

- **GitHub Pages**：新建 Public 仓库，上传 `index.html` 到仓库根目录，再到 Settings → Pages 把 Source 设为 `Deploy from a branch`，分支 `main`、目录 `/(root)`，保存后网址形如 `https://用户名.github.io/仓库名/`。
- **Netlify Drop**：打开 https://app.netlify.com/drop ，把这个文件夹或 `index.html` 拖进去，立即得到公开网址。

两个服务都会提供可以直接发给别人的公网链接。

## 本机预览源码

在 `源文件/` 目录运行：

```sh
npm run dev
```

然后打开 http://127.0.0.1:3000 。需要 Node.js 18 或更新版本，无需安装依赖。运行 `npm run check` 检查 JavaScript 语法。

## 已包含的界面功能

- 输入框下方的模型选择器，支持厂商筛选、搜索和切换。
- 14 个对话模型，包括 GPT-6 Astra、GPT-6.1 Sol、Claude Opus 5.5、Gemini 4 Argon、DeepSeek V4、Qwen 3.8 与 Grok 4.7。
- 图片模型包括 GPT Image 2.5 Sunburst / Flare，以及 Nano Banana 2.1 / 2 Lite / Pro 与经典版。
- 图片尺寸默认 1000 × 2000（1:2），另有 1:1、3:2、2:3、2:1、16:9、9:16 和自定义宽高（128–8192 px 任意整数，自动显示最简比例）。
- 画质选择、生成等待与停止状态、占位预览画布、复制回复、新建对话、历史搜索与浏览器本地记录。
- 文本附件、快捷灵感卡片，以及手机端适配。

模型名称核对于 2026-10-14，仅用于界面展示。
