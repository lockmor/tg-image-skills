# Gemini TG Image Gen Skill for OpenClaw

OpenClaw agent skill: Generate AI images with OpenRouter (Gemini 2.5 Flash) and send directly to Telegram.

## 🚀 Quick Start (Insert Your API Key)

1. **Get OpenRouter API Key:** [openrouter.ai/keys](https://openrouter.ai/keys) → Create free key.

2. **Install Skill:**
   ```
   clawhub install gemini-tg-image-gen
   ```

3. **Set API Key (env):**
   ```
   export OPENROUTER_API_KEY=sk-or-...
   # Or in ~/.bashrc / OpenClaw env
   ```

4. **Test in Agent:**
   ```
   python3 /path/to/skills/gemini-tg-image-gen/scripts/generate_image.py "A cat in space"
   # Outputs: {"paths": ["/tmp/openrouter_image_123.png"]}
   ```

## 📱 Telegram Workflow

```
# 1. Notify
message action=send channel=telegram text="⏳ Generating image..."

# 2. Generate (env must have OPENROUTER_API_KEY)
python3 scripts/generate_image.py "prompt"

# 3. Send
message action=send channel=telegram media="/tmp/openrouter_image_*.png" caption="Generated: prompt"

# 4. NO_REPLY
```

## Files

- [SKILL.md](./gemini-tg-image-gen/SKILL.md)
- [generate_image.py](./gemini-tg-image-gen/scripts/generate_image.py) — No hard-coded keys!

## Security

- **API Key via ENV only** — Insert your own, never commit.
- Public script: Safe to fork/share.

Fork/PR: [github.com/lockmor/tg-image-skills](https://github.com/lockmor/tg-image-skills)

MIT License.