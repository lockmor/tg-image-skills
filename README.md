# Gemini TG Image Gen Skill for OpenClaw

OpenClaw agent skill for AI image generation via OpenRouter (Gemini 2.5 Flash) + send to Telegram.

## Skill

- **gemini-tg-image-gen**: Generate images and send to TG. Uses `OPENROUTER_API_KEY` env var. Script saves PNG locally.  
  [SKILL.md](./gemini-tg-image-gen/SKILL.md) | [generate_image.py](./gemini-tg-image-gen/scripts/generate_image.py)

## Install

```
clawhub install gemini-tg-image-gen
```

## Security

- No hard-coded keys/API secrets.
- Script reads `OPENROUTER_API_KEY` from environment only.

Published on [ClawHub](https://clawhub.com). Fork/PR welcome.

## License

MIT