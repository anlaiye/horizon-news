# Horizon 日报 — AI PM 的每日信息摄入系统

> 42 个信息源 × DeepSeek AI 筛选 × 日报输出到 Obsidian

## 这是什么

基于 [Horizon](https://github.com/recallwei/Horizon) 搭建的 AI 驱动新闻聚合系统。每天自动从 42 个信息源抓取内容，用 DeepSeek 评分筛选，生成结构化中文日报。

## 我的配置

| 项目 | 配置 |
|------|------|
| AI 模型 | DeepSeek (`deepseek-chat`) |
| 评分阈值 | 5.0（默认 7.0，调低以获得更多内容） |
| 信息源 | 42 个，覆盖 8 个领域 |
| 日报输出 | Markdown，自动链接到 Obsidian |
| 运行方式 | `uv run horizon` |

## 信息源领域

- 🤖 AI/ML
- 🐧 Linux
- 🔒 安全
- 🌐 Web 开发
- 💻 编程语言
- 🔧 嵌入式
- 📖 开源
- 🔬 科学

## 日报示例

> 2026-06-15：从 93 条内容中筛选出 24 条重要资讯

涵盖 AI 出口管制、Linux 内核发布、人形机器人、OpenAI 合作伙伴网络等话题。

## 为什么 AI PM 需要这个

1. **AI 领域变化太快** — 每天有几篇重要新闻，只看公众号根本追不上
2. **英文信息是金矿** — 中文 AI 媒体基本是翻译二手，Horizon 直接从 Reddit/HN/LWN 抓一手
3. **自动去噪** — 42 个源每天几百篇文章，AI 评分 < 5 的直接过滤，只看高价值内容
4. **积累行业认知** — 日报存 Obsidian，面试、写文章随时翻出来用

## 快速开始

```bash
# 安装 Horizon
git clone https://github.com/recallwei/Horizon.git
cd Horizon
uv sync

# 配置 AI 模型（用 DeepSeek）
# 编辑 .env 文件，填入你的 API Key
# 编辑 data/config.json，设置评分阈值

# 运行
uv run horizon
```

详见 [Horizon 官方文档](https://github.com/recallwei/Horizon)。
