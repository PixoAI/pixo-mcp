---
name: generate-media
description: Discover Pixo models, estimate credits, generate images, video, speech or music, and retrieve generation results. Use when the user asks to use Pixo or a connected Pixo model for these tasks.
---

# Generate media with Pixo

Use the connected `pixo` MCP. If authentication is required, direct the user to
connect Pixo through the client's plugin settings and sign in with their Pixo
account. Provider keys stay on Pixo servers; generations charge the connected
user's personal Pixo account and follow its subscription restrictions.

## Choose a model and estimate

Call `list_models`, then `get_model` for the selected model. Use the returned
model ID, exact input names, and constraints; the live catalog is authoritative.
Put model-specific parameters in `inputs`. Media references must be accessible
HTTPS URLs or existing Pixo upload keys. Local file paths cannot be submitted;
this MCP has no upload tool.

Call `estimate_cost` with the intended model and inputs before generation, and
disclose the estimated Pixo credits. An estimate is not a spending cap: media
inspection during submission may change the final price. Listing a model does
not guarantee the user's plan can run it.

## Generate and retrieve results

Only call `generate` when the user has requested generation. A request to browse
models or estimate cost does not authorize a paid generation. Follow any budget
or confirmation conditions the user has set.

Each `generate` call creates a new paid request and returns a `generation_id`.
Poll `get_generation` using that ID, with at least five seconds between polls.
Never call `generate` again to check progress. After an ambiguous submission
timeout, ask the user to check Pixo Playground history before submitting again;
this MCP does not provide idempotent retries or a history-listing tool.

When `get_generation` reports a completed result, show it in the conversation
if the matching preview tool is available. For an image, call `preview_pixo_image`.
For a video, call `preview_pixo_video` to show a player. Pass the same generation
ID and call the preview tool once. If the preview is unavailable or fails, share
the original media link from the generation result.

Report the returned job status and use the actual output URLs or text. A pending
job is not a completed generation. If execution fails, explain the returned
error before proposing changes; a new submission is another paid request.
