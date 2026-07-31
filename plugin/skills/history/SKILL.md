---
name: history
description: >-
  Show the most recent entries on the user's braindump tape, newest first — a
  thin pass-through to the braindump MCP history tool. Use when the user runs
  /braindump:history [n] or asks what was recently dumped.
---

# Tape history (pure pass-through)

Call the braindump MCP `history` tool. If the arguments contain a number,
pass it as `limit`; otherwise omit it and take the default. Show the returned
entries as they come back (one line per entry, newest first). Add nothing
beyond formatting.
