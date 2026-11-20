# Pixo MCP

Generate images, videos, spoken audio, and music directly from Claude Code with your Pixo account. Describe what you want to create, and Claude can help you choose a Pixo model, check its inputs, estimate the credit cost, and retrieve the finished result.

## Install in Claude Code

Run these commands in your terminal:

```sh
claude plugin marketplace add PixoAI/pixo-mcp
claude plugin install pixo@pixo-plugins
```

Start a new Claude Code session and open `/mcp`. Select the Pixo server, choose **Authenticate**, sign in with your Pixo account, and select **Allow connection**.

## Try Pixo

Check your connection by listing models without starting a generation:

```text
/pixo:generate-media List Pixo text-to-image models without generating anything.
```

Listing models does not use Pixo credits. The generation prompts below use credits from the connected Pixo account.

Once connected, copy any of these prompts into Claude Code:

| Media | Example prompt |
| --- | --- |
| Image | Generate a studio product photo of a cobalt-blue ceramic mug on a pale pink background with soft side lighting. |
| Video | Generate a five-second clip of a paper boat drifting across a quiet pond, with a slow camera pan. |
| Speech | Turn this line into a warm, conversational voiceover: “Welcome to the studio. Today we're making something new.” |
| Music | Generate a mellow instrumental track with soft piano and brushed drums, with no vocals. |

To get a credit estimate without starting a generation, ask Claude:

```text
Estimate the Pixo credits for the paper boat video before generating it. Wait for my approval.
```

## Connect another MCP client

Add `https://api.pixo.video/mcp/models/` as a remote HTTP MCP server and complete the OAuth prompt in your client.

[Visit Pixo](https://pixo.video) · [Contact support](https://pixo.video/contact)
