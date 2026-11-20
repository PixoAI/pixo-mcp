# Pixo MCP

Use Pixo in Claude Code to discover image, video, speech, and music models, inspect their inputs, estimate credits, and generate media with your Pixo account.

## Install in Claude Code

Run these commands in your terminal:

```sh
claude plugin marketplace add PhotonAISG/pixo-mcp
claude plugin install pixo@pixo-plugins
```

Start a new Claude Code session and open `/mcp`. Select the Pixo server, choose **Authenticate**, sign in with your Pixo account, and select **Allow connection**.

Try a model lookup:

```text
/pixo:generate-media List Pixo text-to-image models without generating anything.
```

Image, video, and audio generation uses your personal Pixo credits. You can ask for an estimate before submitting a generation.

## Connect another MCP client

Add `https://api.pixo.video/mcp/models/` as a remote HTTP MCP server and complete the OAuth prompt in your client.

[Visit Pixo](https://pixo.video) · [Contact support](https://pixo.video/contact)
