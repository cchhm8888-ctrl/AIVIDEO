# Video Breakdown to Brief

从参考影片或原创选题出发，辅助 AIGC 视频的前期创作：故事、一句故事法与双曲线、四拍、分镜、空间调度、资产图提示词、带时间码的关键帧与逐镜视频提示词，以及动态镜头制作记录。支持按阶段交付；不会默认生成实际视频。

这是一个文件式 Agent Skill。`SKILL.md` 是入口；`references/` 是按需读取的规则。安装时请保留整个目录，不要只复制 `SKILL.md`。`agents/openai.yaml` 仅为 Codex 的可选界面元数据，其他智能体可忽略。

## 下载安装

在 GitHub 点击 **Code → Download ZIP** 并解压，或者使用 `git clone`。进入仓库中的 `video-breakdown-to-brief/` 子目录，把**这个子目录整体**复制到目标智能体扫描的 `skills` 目录中。最终应是 `…/skills/video-breakdown-to-brief/SKILL.md`，且 `references/` 与它同级。不要把整个 `AIVIDEO` 仓库目录直接放进 `skills`。

| 智能体 | 用户级安装位置 | 项目级安装位置 |
| --- | --- | --- |
| Codex | `~/.codex/skills/video-breakdown-to-brief/` | `.agents/skills/video-breakdown-to-brief/` |
| DeepSeek Harness | `~/.dsh/skills/video-breakdown-to-brief/` | `.dsh/skills/video-breakdown-to-brief/` |
| Claude Code | `~/.claude/skills/video-breakdown-to-brief/` | `.claude/skills/video-breakdown-to-brief/` |
| Cursor | `~/.cursor/skills/video-breakdown-to-brief/` | `.cursor/skills/video-breakdown-to-brief/` |

Windows 中的 `~` 指当前用户目录，例如 `C:\Users\你的用户名`。安装后开启新会话，在请求中写“使用 `video-breakdown-to-brief`：模式为生成新脚本……”；若目标智能体提供技能列表，也可从列表中调用。不同产品的技能发现和工具能力可能不同；本技能的核心方法与模型、平台无关，但读取视频、图片、生成文件或联网检索仍取决于目标智能体可用的工具。

普通豆包聊天与普通 DeepSeek 网页聊天不是上述文件式技能运行环境，不能仅靠复制目录完成安装。可以把 `SKILL.md` 的相关流程改写为自定义智能体设定，并按平台支持的方式提供 `references/` 内容；这属于提示词移植，不等同于原生 Skill 安装。DeepSeek **Harness** 则支持上述目录安装。

## 使用示例

> 使用 video-breakdown-to-brief，模式：生成新脚本。我想做一支 60 秒、无台词的珠宝故事短片。先完成故事原子、一句故事法、共情与反差、双曲线、情绪钩子和故事节点；我确认后再生成四拍、镜头和提示词。

> 使用 video-breakdown-to-brief。根据我提供的参考片只提取可迁移的叙事节奏和 Style DNA，不复制原片人物、情节或视觉标识。先不要生成完整制作包。

## 目录

```text
video-breakdown-to-brief/
├── SKILL.md
├── references/
│   ├── story-development.md
│   ├── worksheet-schema.md
│   ├── asset-prompt-schema.md
│   ├── w03-style-skill-flow.md
│   └── w05-dynamic-shot-production.md
└── agents/
    └── openai.yaml
```

## 注意

- 参考片时间码只用于拉片证据；新片时间码用于镜头、关键帧和逐镜提示词，不应混用。
- 用户只要求某一阶段时，就停在该阶段，不擅自补齐整套生产包。
- 此仓库只包含技能指令，不包含用户的珠宝素材、参考影片或成片。
- 目前未附开放源代码许可证；如需允许他人修改和再分发，请由仓库所有者选择并添加许可证。

安装位置依据：[DeepSeek Harness 官方说明](https://github.com/deepseek-ai/deepseek-harness/blob/master/packages/skill/skill-filesystem/README.zh.md)、[Cursor 官方说明](https://cursor.com/help/customization/skills)、[Claude Code 官方说明](https://code.claude.com/docs/en/skills)、[Codex Skills 说明](https://developers.openai.com/codex/skills)。
