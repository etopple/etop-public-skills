---
name: news
description: Pull a fresh AI & tech news digest from across the web — model releases, capability jumps, pricing changes, and practical "how to use it" updates. Invoke when the user types /news, asks "what's new in AI", "what did OpenAI/Anthropic/Google ship", "what should I be reading this week". Supports /news today, /news week, /news month, and free-form topics like /news agents.
---

# News Skill — AI & Tech Digest

Replaces the "open 12 tabs every morning" habit with one command: a fast, scannable, link-rich brief on what actually shipped.

> **Customize this skill — this is where the expertise lives.** A generic source list gives generic results. Edit the *Audience* line below and the source list in [`sources.md`](sources.md) to match **your** field: the outlets you trust, the people you follow, and the tools/topics you want flagged. The specifics are what turn a generalist into an expert.

**Audience (edit me):** someone who tracks AI and wants the signal without the noise — model releases, pricing, and practical how-to.

Default tone: terse, scannable, link-rich. No preamble, no fluff. The reader skims.

---

## Invocation

| Input | Behavior |
|---|---|
| `/news` | Full digest, last 7 days |
| `/news today` | Last 24 hours only |
| `/news week` | Last 7 days (default) |
| `/news month` | Last 30 days |
| `/news <topic>` | Free-form topic (e.g. `/news agents`, `/news Anthropic`, `/news open models`) |

Combine freely: `/news today agents`.

---

## Execution flow

1. **Parse args.** Default window = 7 days.
2. **Fan out parallel searches.** Issue all WebSearch / WebFetch calls in a single message — never serial. Aim for 12–15 parallel calls per run.
3. **Dedupe** by headline / URL similarity.
4. **Tag each item** with: source, date, category, and a ★ flag if it's directly relevant to *your* stack (the list you define in `sources.md`).
5. **Synthesize** into the output format below.

Source buckets to hit in parallel live in [`sources.md`](sources.md) — read it when planning the fan-out. At minimum:
- **Official release pages:** the labs you care about (Anthropic, OpenAI, Google, etc.).
- **Practical / how-to trackers:** independent writers who surface what's actually useful.
- **Search:** `"<lab>" release announcement <date>` and `"<topic>" technique <date>`.

---

## ★ Relevance tagging

Flag an item with ★ if it touches something on **your** watch-list (defined in `sources.md`) — a tool you use, a platform you build on, a competitor, a topic you're tracking. For each ★ item, add a one-line **What to do:** (e.g. "Test the new model on our eval set", "Update our MCP config for the new transport").

This filter *is* the expertise. It's the difference between "here's all the news" and "here's what matters to you."

---

## Output format

Keep it terse. No filler.

```
# News digest — <window> (<today's date>)

## AI — releases
- **<Headline>** — <1–2 sentence summary>. [Source](url) · <YYYY-MM-DD>

## AI — practical / how-to
- **<Headline>** — <what it is, why it's useful>. [Source](url) · <YYYY-MM-DD>

## <Your custom category>
- ★ **<Headline>** — <summary>. [Source](url) · <YYYY-MM-DD>
  **What to do:** <one line>

---
**Action shortlist** (★ items only):
1. <action>
```

Rules:
- **Max 5 items per section.** More than that, pick the highest-signal ones.
- **No item without a working source link.** Can't link it → drop it.
- **Date every item.** Can't verify the date → mark `· (date unclear)` and demote.
- **Lead with ★ items** in each section.
- **Action shortlist** only appears if there's at least one ★ item.

---

## What NOT to do

- Don't paraphrase from training data — this is *news*, time-bound. Every claim needs a recent web source.
- Don't include items older than the window unless asked.
- Don't summarize anything you couldn't actually fetch. If the snippet is too thin, drop it rather than guess.
- Don't editorialize or lecture. State what happened, link the source.

---

## Extending the source list

If you say "also check X" during a run, add it to the right bucket for this run and offer to persist it to [`sources.md`](sources.md) for next time.
