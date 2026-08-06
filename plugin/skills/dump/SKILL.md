---
name: dump
description: >-
  Dump knowledge from this session into the user's tilden (their personal
  permanent memory) via the tilden MCP dump tool. Use when the user runs
  /tilden:dump or says to remember/dump something — and proactively, without
  asking, when the session produces something worth keeping: a decision and its
  why, a learning, a gotcha, project state, a milestone reached, or personal
  context the user voiced. Dump as you go at natural milestones and do a final
  pass at session end. Never dump credentials, tokens, keys, or secrets — the
  tape is immutable.
---

# Dump to tilden

Deposit knowledge from this session onto the user's tilden tape via the
`dump` MCP tool. This is their personal brain — one permanent, append-only,
searchable memory shared across all their sessions and agents.

## Invoked with arguments = CLI mode

When run as `/tilden:dump <text>` with arguments, the arguments ARE the
entry: call the `dump` tool with them as given — no distilling, no expansion,
no ceremony — and confirm with the entry id. Everything below governs
proactive dumping during a session, not this pass-through case.

## What tilden does for you (so you don't do it yourself)

- Every dump is stored **verbatim and immutably**, timestamped, then a
  background agent enriches it with a fat keyword pile, resolved dates, and
  topic bindings. **Do not write keyword lists, tags, or headers** — that
  machinery exists server-side.
- **Duplication is a feature.** Dumping something related to an earlier dump is
  fine; never search for or merge prior entries. There is no append-vs-create
  decision — every dump is simply a new entry, and read-time machinery
  organizes recurring topics on its own.
- Timestamps and timezones are handled. If you know the user's current IANA
  timezone, pass it as `tz`; otherwise omit it.

## What to dump — be liberal

Bytes are free and un-findable knowledge is the only failure, so the bar is
low. Dump:

- **Decisions and their why** — what was chosen, what was rejected, the
  constraint that decided it
- **Learnings and gotchas** — anything future-you or a future agent would
  otherwise rediscover the hard way
- **How things work** — mechanisms, invariants, "X only works when Y"
- **Project state and milestones** — what got built, shipped, fixed, or broken
  today (unlike org-memory systems, session progress IS welcome here)
- **Personal context the user voices** — plans, people, feelings, life events.
  This is their private brain; personal is the point.
- **Ownership and rationale** — who/what owns a thing, why it's shaped this way

Multiple topics = multiple dump calls, one topic per entry. Dumping nothing is
still valid when a session genuinely produced nothing — but that's rare.

## How to write an entry

Optimize for a future agent reading it cold:

- **Dense, factual, compressed.** Distill; never paste transcripts or
  play-by-play. A whole session becomes a few sentences of what matters.
- **State lasting facts, not narrative.** "The consent page must upsert the
  grant before approving" — not "we discovered that the consent page…".
- **Identifiers inline.** File paths, function names, flag names, system
  names, people's names — in the prose, where enrichment and search can find
  them.
- **Specifics over pronouns.** Name the project, the person, the system.
- Plain prose. No required structure, no markdown ceremony.

## Hard rule

**Never dump credentials, tokens, API keys, or secrets — of the user's or
anyone else's.** The tape is immutable; a dumped secret can never be unstored.
This is the one filter that survives everything else being liberal.

## Cadence

1. When the user explicitly asks: dump immediately, confirm with the entry id.
2. Proactively: at natural milestones (a decision lands, a bug's cause is
   found, something ships) make the dump call without ceremony — a one-line
   mention that you stored it is enough.
3. Session end or context switch: a final pass — anything meaningful not yet
   dumped, dump now.

Keep the human-facing reply short: what you stored, in a phrase, not a recap.
