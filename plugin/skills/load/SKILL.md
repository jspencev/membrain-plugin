---
name: load
description: >-
  Load context from the user's membrain (their personal permanent memory) via
  the membrain MCP ask tool. Use when the user runs /membrain:load, asks
  "what do I know about X" / "what did I say about X", or when prior context —
  a past decision, project history, a person, a plan — would unblock or
  meaningfully inform the current work. Ask targeted questions, synthesize
  silently, reply with a brief orientation, then get to work.
---

# Load from membrain

Orient yourself using the user's membrain — their permanent memory of past
sessions, decisions, projects, and life context — via the `ask` MCP tool.

## How it works

`ask` is not a keyword search: a retrieval agent on the other side searches
the whole memory (verbatim entries plus derived notes), resolves conflicting
information by recency, and returns a synthesized answer. Treat it like asking
a colleague with perfect recall, not like querying a database. A call may take
a minute; that's normal.

## Behavior

1. Form **one to three targeted questions** around the current topic — not one
   vague mega-question, not a mechanical sweep. Different angles pay off:
   "what was decided about X and why", "what's the current state of X",
   "any gotchas or constraints around X".
2. Call `ask` for each. If an answer surfaces a thread worth pulling (a person,
   a prior decision, an adjacent system), one follow-up ask is fine. Stop when
   oriented — this is judgment, not a checklist.
3. **Synthesize silently.** Load what matters into your working context.
4. Reply briefly: confirm context is loaded, give one or two orientation
   points that matter for the task at hand, then proceed with (or ask about)
   the actual work. Do not output the full research or a long summary unless
   asked.

## When to reach for this unprompted

- The user references something with history you don't have ("the auth
  decision", "what we planned for the trip", "that Marcus situation")
- Starting work on a project the brain likely knows about
- A question where the honest answer is "past-you knew this"

If `ask` returns nothing useful, say so plainly and move on — an empty brain
region is information too, not a failure to route around.
