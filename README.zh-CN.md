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

<p align="center"><img src="assets/hero.webp" width="800" alt="两段视频各取一帧：左为文生视频的虚构腕表产品镜头，右为图生视频的雪夜小木屋场景。由 Beatra AI 生成。"></p>

*两段视频各取一帧：左为文生视频的虚构腕表产品镜头，右为图生视频的雪夜小木屋场景。由 Beatra AI 生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`beatra-ai-video-studio`](skills/beatra-ai-video-studio) | [SKILL.md](skills/beatra-ai-video-studio/SKILL.md) | 1.3.4 |

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

## 效果示例

<p align="center"><img src="assets/preview-1.webp" width="800" alt="4 秒文生视频产品镜头：镜头缓慢推近一块放在湿润黑色石面上的虚构钢制腕表。由 Beatra AI 生成。"></p>

[▶ 观看完整视频（MP4）](assets/full-1.mp4)

*完整 4 秒 1080p 文生视频：柔和轮廓光下湿润黑石上的虚构腕表，带模型生成的环境音。由 Beatra AI 生成。*

提示词：

```text
Cinematic luxury product ad shot. A steel automatic wristwatch with a deep midnight-blue sunburst dial, plain polished baton hour markers, no text and no logos on the dial, lies on a slab of wet black stone covered in small water droplets. Dark studio, soft rim light traces the case edge and bracelet, a gentle highlight glides across the sapphire crystal. The camera makes one slow, steady push-in from a three-quarter view toward the dial; a single water droplet slides slowly down the stone beside the watch. The watch stays perfectly still and keeps its exact shape, the second hand ticks smoothly. Shallow depth of field, crisp macro detail, restrained elegant pacing, ends on a close framing of the dial. Subtle ambient sound of soft water drips.
```

<p align="center"><img src="assets/preview-2.webp" width="800" alt="5 秒图生视频：一张生成的蓝调时刻山间小木屋图片动了起来，雪花飘落、烟囱冒烟、镜头缓慢推近。由 Beatra AI 生成。"></p>

[▶ 观看完整视频（MP4）](assets/full-2.mp4)

*完整 5 秒 720p 图生视频：雪花飘落、烟囱升起炊烟的雪山小木屋，带模型生成的环境音。由 Beatra AI 生成。*

提示词：

```text
Gentle falling snow drifts down across the whole scene in soft, slow flakes. Chimney smoke rises and curls lazily to the left. The window light glows warmly with a faint flicker. The camera makes one slow, smooth push-in toward the cabin. The cabin, roof, pine trees and mountains stay still and keep their exact shape. Calm, quiet winter evening pacing. Soft ambient sound of wind and falling snow.
```

## 规格

截至 2026-10-16。实时列表：https://docs.beatra.ai/zh/docs/models

- **文生图** — 10 个模型（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live）；单次最多 4 张；画布最多 16777216 像素
- **图生图** — 10 个模型（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、MiniMax Image 01 Live）；单次最多 4 张；画布最多 16777216 像素
- **图片编辑** — 6 个模型（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro）；单次最多 4 张；画布最多 4194304 像素
- **文生视频** — 9 个模型（seedance-2-mini、wan2.7-t2v、wan3.0-video、minimax-h3、happyhorse-1.1-t2v、seedance-2-fast、seedance-2、wan3.0-video-prime、seedance-2.5）；480p 至 4K；2–30 秒；画幅 16:9、1:1、21:9、3:4、4:3、9:16、4:5、5:4、9:21；MOV、MP4；2 个带原生音频
- **图生视频** — 9 个模型（wan2.7-i2v、wan3.0-video、minimax-h3、seedance-2-mini、happyhorse-1.1-i2v、seedance-2-fast、seedance-2、wan3.0-video-prime、seedance-2.5）；480p 至 4K；2–30 秒；画幅 16:9、1:1、21:9、3:4、4:3、9:16；MOV、MP4；2 个带原生音频
- **首尾帧生视频** — 8 个模型（wan2.7-i2v、wan3.0-video、minimax-h3、seedance-2-mini、seedance-2-fast、seedance-2、wan3.0-video-prime、seedance-2.5）；480p 至 4K；2–30 秒；画幅 16:9、1:1、21:9、3:4、4:3、9:16；MOV、MP4；2 个带原生音频
- **参考生视频** — 9 个模型（wan2.7-r2v、minimax-h3、wan3.0-video、happyhorse-1.1-r2v、seedance-2-mini、seedance-2-fast、seedance-2、wan3.0-video-prime、seedance-2.5）；480p 至 4K；2–30 秒；画幅 16:9、1:1、3:4、4:3、9:16、21:9、4:5、5:4、9:21；MOV、MP4；2 个带原生音频
- **视频编辑** — 8 个模型（wan2.7-videoedit、wan3.0-video、happyhorse-1.0-video-edit、seedance-2-mini、seedance-2-fast、seedance-2、wan3.0-video-prime、seedance-2.5）；480p 至 4K；2–30 秒；画幅 16:9、1:1、3:4、4:3、9:16、21:9；MOV、MP4
- **视频延长** — 7 个模型（wan2.7-i2v、wan3.0-video、seedance-2-mini、seedance-2-fast、seedance-2、wan3.0-video-prime、seedance-2.5）；480p 至 4K；2–30 秒；画幅 16:9、1:1、21:9、3:4、4:3、9:16；MOV、MP4；1 个带原生音频

## 为什么用 Beatra，而不是直接调用模型 API

- **一个账号用到本 skill 的全部模型** — 文生图 10；图生图 10；图片编辑 6；文生视频 9；图生视频 9；首尾帧生视频 8；参考生视频 9；视频编辑 8；视频延长 7（截至 2026-10-16），一次 Beatra 登录即可使用，不必分别管理各家模型的 key。
- **花不花钱由你决定** — 只有你明确要求这次生成，或批准显示实时积分估算的确认卡后才会付费。
- **先策划，再生成** — skill 先帮你规划、指导和检查，再在 Beatra 上生成。
- **文件可以核验** — `skills/` 下的每个文件都与 cdn.beatra.ai 上的发布归档逐字节一致，每次推送前用 SHA-256 校验。
- **更新由你掌控** — 不含自更新程序；用安装时的工具更新。
- **在你的 Agent 里运行** — Claude Code、Codex、OpenClaw。

## 与同类方案对比

| | Beatra（本 skill） | [scenario-labs/skills](https://github.com/scenario-labs/skills) | [black-forest-labs/skills](https://github.com/black-forest-labs/skills) |
| --- | --- | --- | --- |
| 需要的账号或 key | 一个 Beatra 账号，不需要各家模型的 key | Scenario 账号（OAuth 登录）或 Scenario API key（[出处](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L105)） | BFL API key（[出处](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L160-L166)） |
| 模型 | 文生图 10；图生图 10；图片编辑 6；文生视频 9；图生视频 9；首尾帧生视频 8；参考生视频 9；视频编辑 8；视频延长 7 | Scenario 上的视频模型，包括 MiniMax Hailuo、Gemini Omni、Grok Imagine、Veo、Seedance、Kling、Vidu、Wan、Runway、Luma Ray（[出处](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L262-L277)） | FLUX 3 视频模型，支持原生音频（[出处](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L76)） |
| 花钱前 | 只有你明确要求这次生成，或批准显示实时积分估算的确认卡后才会付费 | 质量检查和模型对比两个 skill 可先 dry-run 试算价格（[出处](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L208-L210)） | `draft: true` 可先出快速的低步数预览，再做完整渲染（[出处](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L108)） |
| 支持的 Agent | Claude Code、Codex、OpenClaw | Claude Code、Cursor、Codex、Copilot 及另外 70 多种编程 Agent（[出处](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L30)） | 编程 Agent（skill 遵循 agentskills.io 规范）；另有 Claude Code 插件（[出处](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L16-L68)） |
| 安装 | `npx skills add beatra-ai/ai-video-generator-skill` | `npx skills add scenario-labs/skills`，再连接 Scenario MCP 服务器（https://mcp.scenario.com/mcp）（[出处](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L89-L105)） | `npx skills add black-forest-labs/skills --skill flux-3-video`（[出处](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L36)） |
| 许可证 | MIT-0 | MIT（[出处](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/LICENSE)） | MIT（[出处](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/LICENSE)） |
| 最近更新 | 随每次发布更新（v1.3.4） | 2026-10-15（[出处](https://github.com/scenario-labs/skills/commit/49dd26e47371163ae0020c7f5627d0993626bfc2)） | 2026-08-26（[出处](https://github.com/black-forest-labs/skills/commit/8907d515b0ac270a988ec7a239add81ee13d6cba)） |

事实核对于 2026-10-16。有误请到 [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/issues) 提 issue。

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

## 更新与安全

自 2026 年 10 月的版本起，本 skill 不再包含自更新程序：它只运行你安装的文件，从不自行替换。
请用安装时的工具更新——`npx skills update beatra-ai-video-studio` 或 `gh skill update beatra-ai-video-studio`。
详见 skill 内的 `references/updates-and-security.md`。

## 许可证

[MIT-0](LICENSE)：可自由使用、修改和再分发，包括商用，无需署名；与这些 skill 在 ClawHub 上的条款一致。

## 相关链接

- 官网 — https://www.beatra.cn
- 文档 — https://docs.beatra.cn
- 控制台 — https://console.beatra.cn
- 给 AI Agent 读的说明 — https://www.beatra.cn/llms.txt（索引）· https://www.beatra.cn/llms-full.txt（全部 skill 合成一个文件）

- 微信小程序 — 国内用户微信扫码使用

<img src="assets/beatra-mini-program-qr.jpg" alt="Beatra 微信小程序码" width="160">
