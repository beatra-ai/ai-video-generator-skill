# AI Video Generator Skill

English | [简体中文](./README.zh-CN.md) | [日本語](./README.ja.md)

> 👉 See also [AI Image Generator Skill](https://github.com/beatra-ai/ai-image-generator-skill)

Generate, animate, edit, and extend short AI videos for ads, product stories, social posts, b-roll, transitions, and cinematic concepts, from inside Claude Code, Cursor, Codex, Windsurf, Cline, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-video-generator-skill) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Generate, animate, edit, and extend short AI videos for ads, product stories, social posts, b-roll, transitions, and cinematic concepts. |
| **Models** | Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Seedance 2.0 Mini, Wan 2.7, Wan 3.0 Video, MiniMax H3, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5, Wan 2.7 Video Edit, HappyHorse 1.0 Video Edit |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="One frame from each clip: a text-to-video product shot of a fictional wristwatch (left) and an image-to-video snowy cabin scene (right). AI-generated with Beatra."></p>

*One frame from each clip: a text-to-video product shot of a fictional wristwatch (left) and an image-to-video snowy cabin scene (right). AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`beatra-ai-video-studio`](skills/beatra-ai-video-studio) | [SKILL.md](skills/beatra-ai-video-studio/SKILL.md) | 1.3.6 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/beatra-ai-video-studio). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/ai-video-generator-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/ai-video-generator-skill beatra-ai-video-studio
```

Or clone this repository and copy `skills/beatra-ai-video-studio` into `~/.claude/skills/` for Claude Code,
`~/.cursor/skills/` for Cursor, `~/.agents/skills/` for Codex, `~/.codeium/windsurf/skills/` for Windsurf,
`~/.cline/skills/` for Cline, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the beatra-ai-video-studio skill from https://github.com/beatra-ai/ai-video-generator-skill (folder skills/beatra-ai-video-studio), then follow its SKILL.md to connect my Beatra account.
```

## Examples

<p align="center"><img src="assets/preview-1.webp" width="800" alt="A 4-second text-to-video product shot: slow push-in on a fictional steel wristwatch resting on wet black stone. AI-generated with Beatra."></p>

[▶ Watch the full video (MP4)](assets/full-1.mp4)

*Full 4-second 1080p text-to-video clip of a fictional wristwatch on wet black stone with soft rim light, with model-generated ambient sound. AI-generated with Beatra.*

Ask your agent:

```text
Make a 4-second cinematic product clip from text: a steel automatic wristwatch with a midnight-blue dial, no text or logos, lying on wet black stone, slow push-in, soft rim light.
```

Prompt:

```text
Cinematic luxury product ad shot. A steel automatic wristwatch with a deep midnight-blue sunburst dial, plain polished baton hour markers, no text and no logos on the dial, lies on a slab of wet black stone covered in small water droplets. Dark studio, soft rim light traces the case edge and bracelet, a gentle highlight glides across the sapphire crystal. The camera makes one slow, steady push-in from a three-quarter view toward the dial; a single water droplet slides slowly down the stone beside the watch. The watch stays perfectly still and keeps its exact shape, the second hand ticks smoothly. Shallow depth of field, crisp macro detail, restrained elegant pacing, ends on a close framing of the dial. Subtle ambient sound of soft water drips.
```

<p align="center"><img src="assets/preview-2.webp" width="800" alt="A 5-second image-to-video clip: a generated still of a mountain cabin at blue hour comes alive with falling snow, chimney smoke, and a slow push-in. AI-generated with Beatra."></p>

[▶ Watch the full video (MP4)](assets/full-2.mp4)

*Full 5-second 720p image-to-video clip of a snowy mountain cabin with falling snow and rising chimney smoke, with model-generated ambient sound. AI-generated with Beatra.*

Ask your agent:

```text
Animate ./cabin-blue-hour.png into a 5-second clip: gentle snow falling across the scene, chimney smoke curling to the left, the window light glowing warmly, and one slow smooth push-in.
```

Prompt:

```text
Gentle falling snow drifts down across the whole scene in soft, slow flakes. Chimney smoke rises and curls lazily to the left. The window light glows warmly with a faint flicker. The camera makes one slow, smooth push-in toward the cabin. The cabin, roof, pine trees and mountains stay still and keep their exact shape. Calm, quiet winter evening pacing. Soft ambient sound of wind and falling snow.
```

## Technical Specifications & Output Limits

As of 2026-10-18. Live list: https://docs.beatra.ai/en/docs/models

- **Uploads** — up to 100 MB per file; the per-model input limits below also apply
- **Text to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): Wan Image 2.7 Pro (up to 4 images per request); GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
- **Image to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Image editing** — 6 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro); PNG; up to 4 images per request; canvas up to 4.2 MP
  - 4.2 MP (2K tier): Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro (up to 4 images per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Text to video** — 9 models (Seedance 2.0 Mini, Wan 2.7, Wan 3.0 Video, MiniMax H3, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 21:9, 3:4, 4:3, 9:16, 4:5, 5:4, 9:21; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
  - Native audio: Wan 2.7, MiniMax H3
- **Image to video** — 9 models (Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 21:9, 3:4, 4:3, 9:16; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
  - Native audio: Wan 2.7, MiniMax H3
- **First and last frames to video** — 8 models (Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 21:9, 3:4, 4:3, 9:16; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
  - Native audio: Wan 2.7, MiniMax H3
- **Reference to video** — 9 models (Wan 2.7, MiniMax H3, Wan 3.0 Video, HappyHorse 1.1, Seedance 2.0 Mini, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 3:4, 4:3, 9:16, 21:9, 4:5, 5:4, 9:21; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
  - Native audio: Wan 2.7, MiniMax H3
- **Video editing** — 8 models (Wan 2.7 Video Edit, Wan 3.0 Video, HappyHorse 1.0 Video Edit, Seedance 2.0 Mini, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 3:4, 4:3, 9:16, 21:9; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
- **Video extension** — 7 models (Wan 2.7, Wan 3.0 Video, Seedance 2.0 Mini, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 21:9, 3:4, 4:3, 9:16; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
  - Native audio: Wan 2.7

## Why use Beatra instead of calling model APIs directly

- **One account for every model this skill uses** — Text to image 10; Image to image 10; Image editing 6; Text to video 9; Image to video 9; First and last frames to video 8; Reference to video 9; Video editing 8; Video extension 7 (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Seedance 2.0 Mini, Wan 2.7, Wan 3.0 Video, MiniMax H3, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5, Wan 2.7 Video Edit, HappyHorse 1.0 Video Edit) (as of 2026-10-18), behind one Beatra sign-in; no keys from individual model providers to manage.
- **You decide what gets paid for** — Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate.
- **Direction before rendering** — the skill plans, directs, and reviews the work, then renders it on Beatra.
- **Files you can verify** — every file under `skills/` matches the release archive on cdn.beatra.ai byte for byte, checked by SHA-256 before each push.
- **Updates you control** — no self-updater; update with the tool you installed it with.
- **Runs in your agent** — Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw.

## How it compares

| | Beatra (this skill) | [ZeroLu/Ultimate-AI-Media-Generator-Skill](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill) | [scenario-labs/skills](https://github.com/scenario-labs/skills) | [black-forest-labs/skills](https://github.com/black-forest-labs/skills) |
| --- | --- | --- | --- | --- |
| Account or key needed | A Beatra account; no model provider keys | A CyberBara API key, stored in ~/.config/cyberbara/api_key ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L68-L76)) | A Scenario account (OAuth) or a Scenario API key ([source](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L105)) | A BFL API key ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L160-L166)) |
| Models | Text to image 10; Image to image 10; Image editing 6; Text to video 9; Image to video 9; First and last frames to video 8; Reference to video 9; Video editing 8; Video extension 7 (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Seedance 2.0 Mini, Wan 2.7, Wan 3.0 Video, MiniMax H3, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5, Wan 2.7 Video Edit, HappyHorse 1.0 Video Edit) | CyberBara video models: Sora 2, Seedance 2.5, Seedance 1, Kling 3.0/2.6/O3, Veo 3.1, Gemini Omni Video, MiniMax H3, HappyHorse 1.0 ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L188-L207)) | Video models on Scenario incl. MiniMax Hailuo, Gemini Omni, Grok Imagine, Veo, Seedance, Kling, Vidu, Wan, Runway, Luma Ray ([source](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L262-L277)) | FLUX 3 video models, with native audio ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L76)) |
| Before spending | Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate | `quote` CLI command returns `estimated_credits` and `can_afford` before submission ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L105-L115)) | Dry-run price estimates in its quality-gate and model-comparison skills ([source](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L208-L210)) | `draft: true` returns a fast low-step preview before a full render ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L108)) |
| Agents | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw | OpenClaw, Claude Code, Codex, Claude Cowork, Cursor, Antigravity ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L31-L36)) | Claude Code, Cursor, Codex, Copilot and 70+ others ([source](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L30)) | Coding agents (skills follow the agentskills.io spec); also a Claude Code plugin ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L16-L68)) |
| Install | `npx skills add beatra-ai/ai-video-generator-skill` | `npx skills add ZeroLu/Ultimate-AI-Media-Generator-Skill --all` ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L60)) | `npx skills add scenario-labs/skills`, then connect the Scenario MCP server (https://mcp.scenario.com/mcp) ([source](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/README.md#L89-L105)) | `npx skills add black-forest-labs/skills --skill flux-3-video` ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L36)) |
| License | MIT-0 | MIT ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/LICENSE)) | MIT ([source](https://github.com/scenario-labs/skills/blob/49dd26e47371163ae0020c7f5627d0993626bfc2/LICENSE)) | MIT ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/LICENSE)) |
| Last updated | Updated with every release (v1.3.6) | 2026-09-08 ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/commit/f28e58f2b9814b2056417377c46f34fd35219702)) | 2026-10-15 ([source](https://github.com/scenario-labs/skills/commit/49dd26e47371163ae0020c7f5627d0993626bfc2)) | 2026-08-26 ([source](https://github.com/black-forest-labs/skills/commit/8907d515b0ac270a988ec7a239add81ee13d6cba)) |

Facts checked on 2026-10-16. Corrections: open an issue in [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/issues).

## What you get

- **Direction before creation** — Clarify the action, camera, pacing, duration, and destination before creating the clip.
- **Use the right starting point** — Begin with words, one opening image, exact boundary frames, creative references, or existing footage.
- **Revise with purpose** — Review the delivered motion and choose one focused edit, extension, or new render.

## Use cases

- **Product videos** — Turn product stories, packshots, and creative references into short demonstration or reveal clips.
- **AI ad video** — Create concise campaign shots around one message, action, and placement.
- **Social clips** — Design short vertical or feed-ready ideas with purposeful pacing and framing.
- **Transitions and reveals** — Define exact first and last images and direct the movement between them.
- **Video edits** — Change a focused visual detail or style in existing footage and review what stayed recognizable.
- **B-roll and continuations** — Create a new supporting shot or add footage directly before or after one existing clip.

## FAQ

### What can I make with Beatra AI Video Studio?

You can create short product, ad, social, b-roll, transition, reveal, and cinematic concept clips from text, images, references, or existing footage.

### Can I start from my own image?

Yes. Use one image as the opening frame, or provide exact first and last images for a directed transition.

### Can it edit or continue existing footage?

Yes. It can make a focused change to one clip or add new footage directly before or after it, then help you review the result.

### Which video model does it use?

It matches the requested inputs and settings to a currently eligible model. If you name a compatible model, that choice is kept.

### Can it make a longer sequence?

It can plan a longer idea shot by shot, create reviewable clips in sequence, and organize the delivered shots for captions, narration, transitions, and timeline assembly.

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update beatra-ai-video-studio` or `gh skill update beatra-ai-video-studio`.
Details: `references/updates-and-security.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

## Links

- Website — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-video-generator-skill
- Docs — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-video-generator-skill
- Console — https://console.beatra.ai
- For AI agents — https://beatra.ai/llms.txt (index) · https://beatra.ai/llms-full.txt (every skill in one file)
