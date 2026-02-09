---
name: gemini-tg-image-gen
description: Generate images via OpenRouter (google/gemini-2.5-flash-image) and send to Telegram. Use when user asks for AI-generated images in TG.
---

# Gemini TG Image Gen (OpenRouter)

## Workflow

1. Notify user: `message action=send channel=telegram text="⏳ Generating image, please wait..."`
2. Run: `python3 scripts/generate_image.py "prompt"`
3. Send image: `message action=send channel=telegram media="/root/.openclaw/workspace/tmp/openrouter_image_*.png" caption="Generated: prompt"`
4. NO_REPLY.

## Usage

Script requires `OPENROUTER_API_KEY` env var. Outputs JSON: `{"paths": ["/path/to/image.png"]}`.

```
python3 scripts/generate_image.py "A cat in space" "google/gemini-2.5-flash-image"
```

## Notes

- Saves to `/root/.openclaw/workspace/tmp`.
- Handles data: URLs and direct downloads.
- No keys in code — env only.