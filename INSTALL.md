# 安装说明：WorkBuddy / Codex / 其他 Agent

本目录是标准 Agent Skill 包：`SKILL.md` + `references/`。  
拷贝**整个文件夹** `weixin-gzh-writing/`，保持内部相对路径不变。

## WorkBuddy

**用户级（推荐，所有项目可用）：**

```text
~/.workbuddy/skills/weixin-gzh-writing/
  ├── SKILL.md
  ├── INSTALL.md
  ├── agents/
  └── references/
```

Windows 示例路径：

```text
C:\Users\<你的用户名>\.workbuddy\skills\weixin-gzh-writing\
```

**项目级：**

```text
<工作区>/.workbuddy/skills/weixin-gzh-writing/
```

装完后：

1. 重启 WorkBuddy，或对话里执行技能重载（若客户端支持 `/reload-skills`）
2. 新对话分别试一次改稿与写稿（话术见 SKILL.md）；两种模式都必须可用
3. 确认 `SKILL.md` 顶部有 `agent_created: true`（便于后续在 WorkBuddy 内迭代）

也可用对话：「把这个本地 skill 装到用户技能目录」并指向本文件夹。

## Codex（OpenAI）

**用户级：**

```text
~/.agents/skills/weixin-gzh-writing/
```

**仓库级（团队共享）：**

```text
<仓库根>/.agents/skills/weixin-gzh-writing/
```

装完后：

- Codex 会自动扫描；不出现则重启 Codex
- 显式调用：`$weixin-gzh-writing` 或 `/skills` 里选中
- 可选元数据：`agents/openai.yaml`（展示名与默认提示）

## Cursor / CodeBuddy

| 工具 | 路径 |
|------|------|
| Cursor 用户级 | `~/.cursor/skills/weixin-gzh-writing/` |
| Cursor 项目级 | `<项目>/.cursor/skills/weixin-gzh-writing/` |
| CodeBuddy 用户级 | `~/.codebuddy/skills/weixin-gzh-writing/` |
| CodeBuddy 项目级 | `<项目>/.codebuddy/skills/weixin-gzh-writing/` |

## 快速自检

装好后发两句（改稿、写稿都要过）：

```text
用 weixin-gzh-writing 改稿。先说明改稿四步，并列出你会输出的章节标题。
```

```text
用 weixin-gzh-writing 写稿。选题：测试。先说明写稿五步；未确认大纲前不要写正文。
```

- 改稿应能列出：诊断表 / 标题 / 摘要 / 完整改写稿 / 排版提示 / 改动说明  
- 写稿应能列出：选题校验 / 素材清单 / 大纲（先停）/ 成稿后的诊断与素材缺口  
若只会润色、或只会其中一种模式，说明 skill 未正确加载。

## 注意

- 不要只拷 `SKILL.md` 而丢掉 `references/`，否则细则读不到
- 同一 `name: weixin-gzh-writing` 不要在多处重复安装多份冲突副本；保留一份主力即可
- 本 skill **不编造**案例与数据；缺素材会停下来提问，这是预期行为
