---
name: cosyvoice-tts
description: 本地普通话女声 TTS（基于 CosyVoice2，完全离线，不联网，不记录）
metadata:
  {
    "openclaw":
      {
        "emoji": "🗣️",
        "os": ["linux"],
        "requires": { "bins": ["cosyvoice-tts"] },
      },
  }
---

# cosyvoice-tts

本地离线普通话女声语音合成，基于阿里 CosyVoice2 模型，全程不联网、不记录。

## 安装

脚本已就绪：`/home/yi/.openclaw/tools/cosyvoice-tts/bin/cosyvoice-tts`

确保 PATH 包含该目录，或直接用完整路径调用。

## 用法

```bash
# 生成 OGG（Telegram 语音消息格式）
cosyvoice-tts -o /tmp/voice.ogg "你想说的话"

# 生成 WAV
cosyvoice-tts -o /tmp/voice.wav "你想说的话"

# 生成 MP3
cosyvoice-tts -o /tmp/voice.mp3 "你想说的话"
```

## 发送语音消息

生成后，在回复中加入 `MEDIA:` 指令即可让 OpenClaw 通过 Telegram 发送语音：

```bash
cosyvoice-tts -o /tmp/voice_reply.ogg "这是一条语音消息"
# 然后在回复中包含：
# MEDIA:/tmp/voice_reply.ogg
```

## 注意

- 首次调用需加载模型（约 3-5 秒），后续调用更快
- OGG/Opus 格式适合 Telegram 语音消息
- 生成速度约 1.5 秒生成 6 秒音频（RTX 5090 加速）
- 参考音频：自带中文女声样本

## TTS 配置

- 参考音频：`/home/yi/dev/CosyVoice/asset/zero_shot_prompt.wav`（中文女声）
- 如需更换声音，替换参考音频即可实现零样本声音克隆
