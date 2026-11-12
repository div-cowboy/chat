---
"@chat-adapter/discord": patch
"@chat-adapter/slack": patch
"@chat-adapter/gchat": patch
---

Quote every line of a Markdown block quote in the Discord, Slack, and Google Chat converters. Each converter used to add the `> ` prefix only to the first line of each block and join blocks with a single newline. Discord then dropped later lines out of the quote, Slack did the same on `response_url` replies, and Google Chat showed the same visual break even though it has no native quote. Now each line gets the prefix, and a lone `>` line separates the blocks.
