---
"@chat-adapter/slack": patch
---

Rotate native Slack streams before cumulative markdown text exceeds Slack's 12,000-character `markdown_text` limit. Age-based rotation still applies, but a long reply can overflow well before the stream expires. The adapter counts text already sent and text still buffered in Slack's ChatStreamer, reserves space to close an open code fence, and prefers a paragraph or line break. A line that still fits in a new segment is kept whole so a link or mention is not split; a single line longer than the limit is split.
