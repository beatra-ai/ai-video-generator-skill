# AI Video Generator Skill

[English](./README.md) | 简体中文

从文字、图片、首尾帧、参考素材或已有片段出发，生成、编辑和延长广告、产品与社交短视频，在 Claude Code、Codex 或 OpenClaw 里直接完成。

> [!IMPORTANT]
> 生成需要 [Beatra](https://beatra.ai) 账号并消耗积分，安装本身不收费。

| 问题 | 回答 |
| --- | --- |
| **能做什么** | 从文字、图片、首尾帧、参考素材或已有片段出发，生成、编辑和延长广告、产品与社交短视频。 |
| **运行要求** | Python 3.10+，以及能加载 `SKILL.md` 的 Agent |
| **费用** | 安装免费。每次生成消耗 Beatra 账号积分，只有你明确要求这次生成或批准确认卡后才会付费。 |
| **支持的 Agent** | Claude Code、Codex、OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`beatra-ai-video-studio`](skills/beatra-ai-video-studio) | [SKILL.md](skills/beatra-ai-video-studio/SKILL.md) | 1.2.5 |

本仓库由 [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/beatra-ai-video-studio) 自动发布，问题请到那里反馈。

## 安装

使用 [`skills`](https://skills.sh) CLI：

```bash
npx skills add beatra-ai/ai-video-generator-skill
```

使用 GitHub CLI：

```bash
gh skill install beatra-ai/ai-video-generator-skill beatra-ai-video-studio
```

也可以克隆本仓库，把 `skills/beatra-ai-video-studio` 复制到 `~/.claude/skills/`（Claude Code）、`~/.agents/skills/`（Codex）或 `~/.openclaw/skills/`（OpenClaw）。

或者把下面这段话发给你的 Agent：

```text
从 https://github.com/beatra-ai/ai-video-generator-skill 安装 beatra-ai-video-studio skill（目录 skills/beatra-ai-video-studio），然后按它的 SKILL.md 连接我的 Beatra 账号。
```

## 你能得到什么

- **先定方向，再制作** — 先明确动作、运镜、节奏、时长与发布场景，让镜头意图更清楚。
- **按素材选择起点** — 可以从文字、开场图、首尾帧、参考素材或已有视频开始。
- **有针对性地改进** — 查看生成结果中的动作与稳定性，再选择一次针对性修改、延长或重新生成。

## 适用场景

- **产品视频** — 把产品故事、产品图和创意参考变成简洁的演示或揭示镜头。
- **AI广告视频** — 围绕一个信息、一个动作和一个投放位置制作短片。
- **社交短视频** — 按竖屏或信息流场景安排节奏、画幅与开场。
- **转场与揭示** — 指定首尾两张画面，设计它们之间的运动。
- **视频修改** — 针对已有片段修改一个画面细节或风格，并检查需要保留的重点内容。
- **空镜与续拍** — 制作新的辅助镜头，或在一段已有视频之前或之后增加画面。

## 常见问题

### Beatra AI视频工作室可以制作什么？

可以从文字、图片、参考素材或已有视频制作产品、广告、社交、空镜、转场、揭示和电影感概念短片。

### 可以从自己的图片开始吗？

可以。可以把一张图片作为开场画面，也可以提供准确的首尾两张图片来设计转场。

### 可以修改或续拍已有视频吗？

可以。可以只修改一段视频里需要调整的部分，或在它之前或之后增加新画面，再查看生成结果。

### 它会使用哪个视频模型？

它会根据输入素材和创作要求选择当前适用的模型；如果你指定的模型适合这项制作，就会继续使用它。

### 可以制作更长的内容吗？

可以逐镜规划较长内容，按顺序生成并交付多段短片，方便继续安排字幕、旁白、镜头转场和时间线合成。

## 更新

安装后的 skill 每天最多检查一次新版本，替换前先校验官方归档，任何一步失败都不会动你已安装的版本。
随时可以关闭，见 skill 内的 `references/automatic-updates-and-safety.md`。

## 许可证

[MIT-0](LICENSE)：可自由使用、修改和再分发，包括商用，无需署名；与这些 skill 在 ClawHub 上的条款一致。
