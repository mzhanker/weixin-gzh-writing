# weixin-gzh-writing

微信公众号 **写稿 / 改稿** Agent Skill。按微信推荐结构执行：分型诊断、标题开头、评论区、关注收藏与 SEO。

## 能力

| 模式 | 做什么 |
|------|--------|
| **改稿** | 不损伤原意与语气，重构分发结构 |
| **写稿** | 选题校验 → 素材清单 → 大纲确认 → 成稿 |

两种模式同等支持，由同一 Agent 一次对话完成。不做发后复盘。

## 安装

拷贝整个 `weixin-gzh-writing/` 目录（勿只拷 `SKILL.md`）：

| 工具 | 路径 |
|------|------|
| Cursor | `~/.cursor/skills/weixin-gzh-writing/` 或项目 `.cursor/skills/` |
| WorkBuddy | `~/.workbuddy/skills/weixin-gzh-writing/` |
| Codex | `~/.agents/skills/weixin-gzh-writing/` |

详见 [INSTALL.md](INSTALL.md)。

## 目录结构

```text
weixin-gzh-writing/
├── SKILL.md
├── INSTALL.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    ├── algorithm.md
    ├── type-rules.md
    ├── comment-type.md
    ├── redlines.md
    ├── rewrite-workflow.md
    └── write-workflow.md
```

## 快速触发

**改稿：**

```text
用 weixin-gzh-writing 改稿。先判定类型并打分，指出最弱两项；
给 3 标题 + 120 字摘要 + 完整改写稿 + 排版提示 + 改动说明。
```

**写稿：**

```text
用 weixin-gzh-writing 写稿。选题：（一句话）
先选题校验 → 素材清单 → 大纲等我确认 → 确认后再写正文。
```

## 协议

[MIT License](LICENSE) — 可自由使用、修改与商用；再分发时请保留版权与许可声明。

## 仓库

https://github.com/mzhanker/weixin-gzh-writing
