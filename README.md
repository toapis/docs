<p align="center">
  <a href="https://toapis.com"><strong>Website</strong></a> •
  <a href="https://docs.toapis.com"><strong>Documentation</strong></a> •
  <a href="https://toapis.com/console/token"><strong>API Keys</strong></a> •
  <a href="https://docs.toapis.com/docs/en/quickstart"><strong>Quickstart</strong></a>
</p>

# ToAPIs Documentation

Official documentation for [ToAPIs](https://toapis.com), a unified AI API gateway that provides OpenAI-compatible chat plus async image and video generation across leading model providers.

## Supported APIs

| Category | What's covered | Docs |
| --- | --- | --- |
| **Chat** | OpenAI-compatible completions, Anthropic Messages, OpenAI Responses, streaming, structured output, and tool calling. GPT-5, Claude, DeepSeek, Gemini, Qwen, Kimi, GLM, MiniMax. | [API reference](https://docs.toapis.com/docs/en/api-reference/chat/chat) |
| **Image** | Text-to-image and reference-image generation. GPT-Image-2, GPT-4o, Gemini, Seedream, Flux, Grok Image. | [API reference](https://docs.toapis.com/docs/en/api-reference/images/gpt-image-2/generation) |
| **Video** | Text/image-to-video generation. Veo 3, Sora 2, Kling, Wan, MiniMax Hailuo, Seedance, Gemini Omni Flash. | [API reference](https://docs.toapis.com/docs/en/api-reference/videos/sora2/generation) |
| **Platform** | Async task status, uploads, rate limits, webhooks, and account / API-key management. | [Webhooks](https://docs.toapis.com/docs/en/api-reference/webhooks/task-webhooks) |

## Quickstart

```bash
curl https://toapis.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model": "gpt-5.6-terra", "messages": [{"role": "user", "content": "Hello"}]}'
```

Create an API key at [toapis.com/console/token](https://toapis.com/console/token), then follow the full [quickstart guide](https://docs.toapis.com/docs/en/quickstart).

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

## Links

- [Website](https://toapis.com)
- [Documentation](https://docs.toapis.com)
- [Dashboard / API Keys](https://toapis.com/console/token)

## License

See [LICENSE](./LICENSE) for details.
