# TG Image Skills for OpenClaw

OpenClaw agent skills for generating and sending images to Telegram.

## Skills

- **tg-image-sender**: Send test images (Picsum) or custom media to Telegram chats via `message` tool. No API keys.  
  [SKILL.md](./tg-image-sender/SKILL.md)

- **gemini-tg-image-gen**: AI image generation via OpenRouter (Gemini 2.5 Flash) + send to TG. Uses `OPENROUTER_API_KEY` env var. Script saves PNG locally.  
  [SKILL.md](./gemini-tg-image-gen/SKILL.md) | [generate_image.py](./gemini-tg-image-gen/scripts/generate_image.py)

## Install

```
clawhub install tg-image-sender
clawhub install gemini-tg-image-gen
```

## Security

- No hard-coded keys/API secrets.
- Gemini script reads `OPENROUTER_API_KEY` from environment only.
- Picsum: Public random images, no auth.

Published on [ClawHub](https://clawhub.com). Fork/PR welcome.

## License

MIT