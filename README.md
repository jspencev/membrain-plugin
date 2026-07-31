# braindump plugin

Claude Code plugin for [braindump](https://api-production-599b.up.railway.app) — a
permanent, personal memory your agents can write to and recall from.

## Install

```
/plugin marketplace add jspencev/braindump-plugin
/plugin install braindump@braindump
```

First tool use opens a browser OAuth flow (sign in with Google, choose full or
dump-only access). One install ships:

- the **remote MCP connection** (`dump` / `ask` / `history` tools)
- **`/braindump:dump`** — distills session knowledge onto your permanent tape;
  fires proactively at milestones; never dumps secrets
- **`/braindump:load`** — asks your brain targeted questions and loads the
  answers as working context

Dumps are stored verbatim on an append-only tape and enriched automatically
(keywords, resolved dates, topic bindings) — the skills stay simple on purpose.
