---
name: gemini-tg-image-gen
description: Generate AI images via OpenRouter Gemini 2.5 Flash + send to Telegram + auto-cleanup. Set OPENROUTER_API_KEY env and run!
---

# Gemini TG Image Gen

## Quick Setup

1. `export OPENROUTER_API_KEY=sk-or-your-key`
2. `clawhub install gemini-tg-image-gen`

## Workflow (with Auto-Cleanup)

```
message action=send channel=telegram text="⏳ Generating..."

python3 scripts/generate_image.py "A futuristic city"

message action=send channel=telegram media="/root/.openclaw/workspace/tmp/openrouter_image_*.png" caption="AI Generated"

rm /root/.openclaw/workspace/tmp/openrouter_image_*.png

NO_REPLY
```

Model: `google/gemini-2.5-flash-image` (default).

No keys in code — env only! Auto-deletes temp PNG after send.