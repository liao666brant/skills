# skills

个人 Agent Skills 仓库，符合 [skills.sh](https://skills.sh) 规范。

技能基于 [Anthropic Agent Skills](https://agent-sdk.anthropic.com/skills) 规范编写（目录 + `SKILL.md` frontmatter），兼容 Claude Code、Codex、OpenCode 等支持该规范的 agent。

## 技能列表

| 技能          | 说明                                                              |
| ------------- | ----------------------------------------------------------------- |
| [git-commit](skills/git-commit/SKILL.md)    | 智能 Git 提交：conventional commits、自动语言检测、可指定语言     |
| [commit-zh](skills/commit-zh/SKILL.md)     | 中文 Git 提交：分析变更并生成中文 conventional commit message     |
| [image-analyzer](skills/image-analyzer/SKILL.md) | 分析图片并支持视觉任务，主模型不能读图时使用可用视觉模型   |
| [code-review](skills/code-review/SKILL.md) | 默认审查未提交改动，也可双轴审查指定基线后的仓库规范与需求实现   |
| [simplify](skills/simplify/SKILL.md) | 保持行为不变地简化代码，改善可读性，默认聚焦近期改动 |
| [review-fix-goal](skills/review-fix-goal/SKILL.md) | 自包含的跨宿主审查修复闭环，最终复审清零后中文提交并推送       |
| [skill-doctor](skills/skill-doctor/SKILL.md) | 基于本地真实 Agent 会话评估技能效果并生成改进报告 |
| [update-skill](skills/update-skill/SKILL.md) | 创建或改进通用 Agent Skill 的结构、触发描述与工作流指令 |
| [optimize-agent-instructions](skills/optimize-agent-instructions/SKILL.md) | 审计和优化 Skill、AGENTS.md 等指令，保留功能契约并减少无关上下文 |
| [unslop](skills/unslop/SKILL.md) | 清除文本中的 AI 腔、套话和机械结构，保留自然语气与作者个性 |
| [show-me](skills/show-me/SKILL.md) | 用精简图示、代码结构草图和 HTML 解释复杂主题 |
| [index-project](skills/index-project/SKILL.md)  | 创建 AGENTS.md 项目与模块索引，代码变更影响索引时主动同步 |
| [writing-for-agents](skills/writing-for-agents/SKILL.md) | 为 Agent 编写低上下文负担、触发清晰且过程稳定的指令文档 |
| [ux-writing](skills/ux-writing/SKILL.md) | 用户可见文案与文档的清晰度、一致性与时效性检查 |
| [clear-writing](skills/clear-writing/SKILL.md) | 统一人类文档、Agent 文档与文案写作，清理套话并核对事实、执行条件和产品输出 |
| [scoped-change](skills/scoped-change/SKILL.md) | 界定变更边界，避免超范围改动与遗漏必要位置 |
| [wsl-windows-image](skills/wsl-windows-image/SKILL.md) | WSL 中读取 Windows 图片：自动转换 /mnt/<盘符>/ 路径并读图            |

## 来源与许可

- `simplify`：中文化并优化自 [oh-my-opencode-slim 随附的 simplify](https://github.com/alvinunreal/oh-my-opencode-slim/blob/2fc0ea82d1a529f1f105513603d8a0847826c112/src/skills/simplify/SKILL.md)，原技能来自 Addy Osmani 的 [code-simplification](https://github.com/addyosmani/agent-skills/blob/be4e44a9fbc5e8df0beaefadbb28bd22ee61cc39/skills/code-simplification/SKILL.md)，遵循 [MIT 许可](https://github.com/addyosmani/agent-skills/blob/be4e44a9fbc5e8df0beaefadbb28bd22ee61cc39/LICENSE)。
- `optimize-agent-instructions`：整理自本仓库的指令优化实践，参考 Eric Provencher 的 [Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra)。
- `ux-writing`：改编自 [scarletkc/agents 的 ux-writing](https://github.com/scarletkc/agents/tree/main/skills/ux-writing)，原作者 [scarletkc](https://github.com/scarletkc)，遵循 Apache-2.0 许可。
- `scoped-change`：改编自 [scarletkc/agents 的 scoped-change](https://github.com/scarletkc/agents/tree/main/skills/scoped-change)，原作者 [scarletkc](https://github.com/scarletkc)，遵循 Apache-2.0 许可。
- `skill-doctor`：中文化并适配自 [warpdotdev/common-skills 的 skill-doctor](https://github.com/warpdotdev/common-skills/tree/69b4753651ab7fab518c82be087b9f1d5b966631/.agents/skills/skill-doctor)，原作者 Denver Technologies, Inc.，遵循 MIT 许可。
- `update-skill`：中文化并适配自 [warpdotdev/common-skills 的 update-skill](https://github.com/warpdotdev/common-skills/tree/main/.agents/skills/update-skill)，原作者 Denver Technologies, Inc.，遵循 MIT 许可。
- `unslop`：中文化并适配自 [Cursor plugins 的 pstack/unslop](https://github.com/cursor/plugins/tree/e8d856f0273b42ebafe0ec3546bd645709e7c1b0/pstack/skills/unslop)，原作者 Lauren Tan，遵循 MIT 许可。
- `show-me`：中文化并适配自 [HumanLayer skills 的 show-me](https://github.com/humanlayer/skills/tree/main/plugins/show-me/skills/show-me)，原作者 HumanLayer，遵循 MIT 许可。
- `writing-for-agents`：中文化并适配自 [mattpocock/skills 的 writing-for-agents](https://github.com/mattpocock/skills/tree/main/skills/productivity/writing-for-agents)，原作者 Matt Pocock，遵循 MIT 许可。
- `clear-writing`：整合本仓库的 `writing-for-agents`、`ux-writing` 和 `unslop`。保留上述来源与作者归属；`writing-for-agents`、`unslop` 部分遵循 MIT 许可，`ux-writing` 部分遵循 Apache-2.0 许可。

## 安装

```bash
npx skills add liao666brant/skills -g
```

`skills` CLI 会自动发现仓库 `skills/` 下的所有技能，并按当前 agent 写入对应的用户级 skills 目录（Claude Code、Codex、OpenCode 等），一套技能多端通用。

## 目录结构

```
skills/
├── skills.sh.json          # skills.sh 展示分组配置
└── skills/                 # 技能目录
    ├── git-commit/
    │   └── SKILL.md
    ├── commit-zh/
    │   └── SKILL.md
    ├── image-analyzer/
    │   └── SKILL.md
    ├── code-review/
    │   ├── SKILL.md
    │   └── agents/
    │       └── openai.yaml
    ├── simplify/
    │   └── SKILL.md
    ├── review-fix-goal/
    │   ├── SKILL.md
    │   ├── agents/
    │   │   └── openai.yaml
    │   └── references/          # review.md / commit.md
    ├── skill-doctor/
    │   ├── SKILL.md
    │   ├── agents/
    │   │   └── openai.yaml
    │   ├── assets/
    │   ├── references/
    │   ├── scorers/
    │   └── scripts/
    ├── update-skill/
    │   ├── SKILL.md
    │   ├── agents/
    │   │   └── openai.yaml
    │   └── references/
    │       └── best-practices.md
    ├── optimize-agent-instructions/
    │   └── SKILL.md
    ├── unslop/
    │   ├── SKILL.md
    │   └── agents/
    │       └── openai.yaml
    ├── show-me/
    │   ├── SKILL.md
    │   └── agents/
    │       └── openai.yaml
    ├── index-project/
    │   ├── SKILL.md
    │   └── references/          # first-index.md / incremental-index.md
    ├── writing-for-agents/
    │   ├── SKILL.md
    │   ├── agents/
    │   │   └── openai.yaml
    │   └── references/
    │       └── skill-mechanics.md
    ├── ux-writing/
    │   └── SKILL.md
    ├── clear-writing/
    │   ├── SKILL.md
    │   ├── agents/
    │   │   └── openai.yaml
    │   └── references/          # human-writing / product-output / agent-writing / skill-mechanics
    ├── scoped-change/
    │   └── SKILL.md
    └── wsl-windows-image/
        └── SKILL.md
```

## 添加新技能

1. 在 `skills/` 下新建目录，目录名即技能名（kebab-case）
2. 编写 `SKILL.md`，frontmatter 必须包含 `name` 和 `description`（description 决定触发时机）
3. 按需在技能目录内放脚本、参考文件等，随技能一起安装
