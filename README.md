# ai-profile · 个人 AI 档案

一份**给 AI 看的个人使用说明**：让不同的 AI 工具都能用我习惯的方式跟我协作。

核心思路是**一份主档案 + 多个轻量入口**：所有实质信息只写在 `PROFILE.md`，其余文件只负责「指路」。这样只改一处，所有 AI 看到的都是最新版，不会出现「这个 AI 知道、那个 AI 不知道」。

## 文件说明

| 文件 | 作用 | 谁会读 |
| --- | --- | --- |
| `PROFILE.md` | ★ 主档案，唯一数据源 | 所有 AI、你自己 |
| `profile.yaml` | 结构化镜像，供程序 / API 消费 | 脚本、自动化、MCP |
| `AGENTS.md` | 指向主档案 | Codex、通用 coding agent |
| `CLAUDE.md` | 指向主档案 | Claude Code |
| `GEMINI.md` | 指向主档案 | Gemini CLI |
| `llms.txt` | 通用 LLM 抓取索引 | ChatGPT、Claude 网页版等 |

## 怎么让一个 AI 用上它

**最通用（推荐）**：把下面这句话发给任何 AI：

```text
请先读取 https://raw.githubusercontent.com/sunjunwen1987/ai-profile/main/PROFILE.md ，并按其中的约定与我协作。
```

**clone 到本地**：

```bash
git clone https://github.com/sunjunwen1987/ai-profile.git
```

然后在项目里把 `PROFILE.md` 加进上下文；支持 `AGENTS.md` / `CLAUDE.md` / `GEMINI.md` 的工具会自动找到对应入口。

**ChatGPT / Claude 网页版**：把主档案内容粘贴到「自定义指令 / Custom Instructions / Project knowledge」里。

**作为网站发布**：`llms.txt` 遵循 https://llmstxt.org 约定，可放在站点根目录供 LLM 抓取。

## 怎么更新

1. 只改 `PROFILE.md`（若改了结构化字段，同步改 `profile.yaml`）。
2. **不要**把内容复制进各个入口文件 —— 它们永远只写「去读 PROFILE.md」。
3. 更新 `PROFILE.md` 顶部的版本号与日期，并在文末版本记录里加一行。

## 隐私说明

本仓库是**公开**的，因此只放偏好类信息（语言、语气、工具、协作习惯），**不放**真实姓名、城市、公司、联系方式或任何敏感信息。任何人都能通过 raw 链接读取，请勿在此添加隐私内容。

## 维护

- 由本人与 WorkBuddy 共同维护
- 初始版本：v1.0（2026-11-23）
