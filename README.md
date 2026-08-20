<p align="center">
  <a href="https://toapis.com"><strong>Website</strong></a> •
  <a href="https://docs.toapis.com"><strong>Documentation</strong></a> •
  <a href="https://toapis.com/console/token"><strong>API Keys</strong></a> •
  <a href="https://docs.toapis.com/docs/en/quickstart"><strong>Quickstart</strong></a>
</p>

# ToAPIs Documentation

Official documentation for [ToAPIs](https://toapis.com), a unified AI API gateway that provides OpenAI-compatible chat plus async image and video generation across leading model providers. One API key gives you access to GPT-5, Claude, Gemini, DeepSeek, and other models with unified pricing and billing.

## Features

- **OpenAI-compatible** — reuse the OpenAI SDK by changing `base_url` to `https://toapis.com/v1`
- **Multiple chat formats** — Chat Completions, Anthropic Messages, and OpenAI Responses
- **Streaming** — Server-Sent Events (SSE) for token-by-token output
- **Vision input** — send images alongside text to vision-capable models
- **Async image & video generation** — submit a task, poll or receive a webhook when it completes
- **Reference-image generation** — image-to-image via `reference_images` / `image_urls`
- **Character references** — reuse characters in video prompts via `@username`
- **Webhooks** — HMAC-SHA256 signed callbacks for async task completion
- **Uploads** — upload local images and videos to obtain URLs for generation
- **Multi-language docs** — English, 简体中文, 繁體中文, 日本語, 한국어, Русский

## Supported APIs

| Category | What's covered | Docs |
| --- | --- | --- |
| **Chat** | OpenAI-compatible completions, Anthropic Messages, OpenAI Responses, streaming, and vision input. GPT-5.6, Claude Fable 5, Claude Opus 5, Claude Sonnet 5, Claude Haiku 4.5, Gemini 3.7 Flash, DeepSeek V4, GLM-5.3, Kimi K3, MiniMax M3, Qwen3.8-Max. | [API reference](https://docs.toapis.com/docs/en/api-reference/chat/chat) |
| **Image** | Text-to-image and reference-image generation. GPT-Image-2, GPT-Image-2 VIP, GPT-4o, Gemini 3 Pro Image, Seedream 5.0 Pro, FLUX 3, Grok Imagine 2.0, Vidu Q2. | [API reference](https://docs.toapis.com/docs/en/api-reference/images/gpt-image-2/generation) |
| **Video** | Text/image-to-video generation. Veo 3.1, Sora 2, Kling 3, Wan 3.0, MiniMax Hailuo 3.0, Seedance 2.5, Gemini Omni Flash, Grok Video 1.5, ViduQ3, HappyHorse 1.1. | [API reference](https://docs.toapis.com/docs/en/api-reference/videos/sora2/generation) |
| **Platform** | Async task status, uploads, rate limits, webhooks, account & API-key management. | [Webhooks](https://docs.toapis.com/docs/en/api-reference/webhooks/task-webhooks) |

## Quickstart

Create an API key at [toapis.com/console/token](https://toapis.com/console/token).

### Chat

```bash
curl https://toapis.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model": "gpt-5.6-terra", "messages": [{"role": "user", "content": "Hello"}]}'
```

### Image generation

```bash
curl https://toapis.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model": "gpt-image-2", "prompt": "A cute panda with cinematic lighting", "size": "1:1", "resolution": "1k", "n": 1}'
```

### Video generation

```bash
curl https://toapis.com/v1/videos/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model": "sora-2-vvip", "prompt": "Waves crashing against the shore", "duration": 12, "aspect_ratio": "16:9"}'
```

Follow the full [quickstart guide](https://docs.toapis.com/docs/en/quickstart) for task polling, streaming, and webhooks.

## Authentication

All endpoints require a Bearer token:

```bash
Authorization: Bearer YOUR_API_KEY
```

Get your key at [toapis.com/console/token](https://toapis.com/console/token). See [account & token docs](https://docs.toapis.com/docs/en/api-reference/account/create-token).

## Integrations

Use ToAPIs from your favorite tools:

- [Claude Code](https://docs.toapis.com/docs/en/integrations/claude-code)
- [Codex](https://docs.toapis.com/docs/en/integrations/codex)
- [Cherry Studio](https://docs.toapis.com/docs/en/integrations/cherry-studio)
- [Chatbox](https://docs.toapis.com/docs/en/integrations/chatbox)
- [OpenClaw](https://docs.toapis.com/docs/en/integrations/openclaw)

## Languages

This documentation is available in:

[English](https://docs.toapis.com/docs/en) · [简体中文](https://docs.toapis.com/docs/cn) · [繁體中文](https://docs.toapis.com/docs/zh-Hant) · [日本語](https://docs.toapis.com/docs/ja) · [한국어](https://docs.toapis.com/docs/ko) · [Русский](https://docs.toapis.com/docs/ru)

## Development

```bash
# Install Mintlify CLI
npm i -g mintlify

# Start local preview
mintlify dev
```

## Resources

- [Website](https://toapis.com)
- [Documentation](https://docs.toapis.com)
- [Dashboard / API Keys](https://toapis.com/console/token)

## License

See [LICENSE](./LICENSE) for details.
