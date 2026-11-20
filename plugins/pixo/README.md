# Pixo for Claude Code

Use Pixo to find models for images, video, speech, and music from a Claude Code session. You can browse the model catalog, inspect a model's inputs, and estimate the credits a request will use before starting a generation.

## Connect your Pixo account

In a new Claude Code session, open `/mcp`, select **Pixo**, and choose **Authenticate**. Sign in to Pixo in your browser and select **Allow connection**.

To check that the connection works, ask Claude to list Pixo text-to-image models without generating anything.

```text
/pixo:generate-media List Pixo text-to-image models without generating anything.
```

Generation uses credits from the connected Pixo account. You can ask for a credit estimate before requesting an image, video, or audio generation.

[Visit Pixo](https://pixo.video) · [Contact support](https://pixo.video/contact)
