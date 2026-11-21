# Pixo for OpenAI

Generate images, videos, speech, and music with your Pixo account. The plugin can list available models, check their inputs, estimate credits, and retrieve generation results. Generations use credits from your connected Pixo account.

## Install in Codex

```sh
codex plugin marketplace add PixoAI/pixo-mcp
codex plugin add pixo@pixo-plugins
```

Sign in to Pixo and allow the connection when prompted. To check the connection without using credits, ask Codex to list Pixo text-to-image models without generating anything.

## Package for OpenAI submission

From this plugin directory, create a ZIP with the manifest and MCP configuration at the archive root.

```sh
zip -r /tmp/pixo-openai-0.1.1.zip .codex-plugin .mcp.json assets skills README.md
```

[Website](https://pixo.video) · [Support](https://pixo.video/contact) · [Privacy](https://pixo.video/privacy)
