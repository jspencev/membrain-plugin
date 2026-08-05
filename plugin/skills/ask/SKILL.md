---
name: ask
description: >-
  Ask the user's membrain (their personal permanent memory) a question and
  relay the answer — a thin pass-through to the membrain MCP ask tool. Use
  when the user runs /membrain:ask <question> or wants a direct answer from
  their brain. For loading working context into the current session, prefer
  the load skill.
---

# Ask the brain (pure pass-through)

Call the membrain MCP `ask` tool with the user's arguments as the question,
verbatim. Pass the user's current IANA timezone as `tz` if known. Do not
rephrase the question or pad it with session context — the point is CLI-like
directness.

The call may take a minute or two; a retrieval agent searches the whole
memory before answering. Relay the answer faithfully and completely — light
formatting is fine, added interpretation is not.

If invoked with no arguments, ask the user what the question is.
