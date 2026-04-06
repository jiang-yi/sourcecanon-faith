# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

## TTS（本地语音合成）

**当前使用：Edge TTS**
- 默认语音：zh-CN-XiaoxiaoNeural（温柔女声）
- 支持中文普通话

```bash
# 生成语音
uv run --with edge-tts python3 -c "
import edge_tts, asyncio
async def gen():
    c = edge_tts.Communicate('你的文字', 'zh-CN-XiaoxiaoNeural')
    await c.save('/tmp/voice.mp3')
asyncio.run(gen())
"
```

**备用：cosyvoice-tts** — 本地离线中文女声

```bash
# 生成语音并通过 Telegram 发送
cosyvoice-tts -o /tmp/voice_reply.ogg "你好，我是小依。"
MEDIA:/tmp/voice_reply.ogg
```

- 脚本路径：`/home/yi/.openclaw/tools/cosyvoice-tts/bin/cosyvoice-tts`
- 支持格式：`.ogg`（Telegram 语音）、`.wav`、`.mp3`
- 生成速度：~1.5s 生成 6s 音频
- 声音：中文女声（CosyVoice2 零样本克隆）

用户要求"语音回复"时，生成 OGG 并附上 `MEDIA:` 行。

---

Add whatever helps you do your job. This is your cheat sheet.
