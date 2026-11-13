---
"@chat-adapter/slack": patch
---

When Slack expires a native stream segment during a long gap, update that message with the markdown Slack had already confirmed. That turns the sealed stream into a normal message and clears the "Something went wrong" error Slack shows when a stream is never stopped. Open task cards on the expired message are replaced by the snapshot and still replay into the next segment. Unconfirmed text still continues in a new message, and a failed update does not change that recovery.
