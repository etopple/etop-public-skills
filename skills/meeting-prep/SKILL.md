---
name: meeting-prep
description: Build a one-page brief before a meeting — who you're meeting, their company, recent news, likely priorities, and smart questions to ask. Invoke when the user types /prep, says "I have a meeting with X", "prep me for my call with Y", or "what should I know before meeting Z". Researches the web and returns a structured, sourced brief.
---

# Meeting Prep Skill

Turns a name and/or company into a tight pre-meeting brief, so you walk in informed instead of winging it.

> **Customize this skill.** Edit the *What I care about* note and the output sections to match your role — a salesperson, a founder, a partner-manager, and a job candidate each want a different brief. Tell the skill who you are and it tailors the angle.

**What I care about (edit me):** *e.g. "I run sales — surface buying signals, budget hints, and a warm way in."*

---

## Invocation

| Input | Behavior |
|---|---|
| `/prep <person> at <company>` | Full brief on person + company |
| `/prep <company>` | Company-only brief |
| `/prep <person>, <role> — <context>` | Tailored brief (add meeting type: sales, partnership, interview, renewal) |

---

## Process

1. **Parse** who and what. Note the meeting type if given.
2. **Fan out parallel web searches** — never serial:
   - the **person** (current role, background, recent public posts/talks),
   - the **company** (what they do, size, model, recent news / funding / launches),
   - the **context** (their market, obvious competitors).
3. **Use only sourced facts.** Mark anything you can't confirm as `UNVERIFIED`. Never fabricate a title, number, or quote.
4. **Synthesize** into the brief below. Lead with what matters; cut the rest.

## Sources to hit (parallel)

- Company site: About, blog, newsroom, pricing, careers.
- `WebSearch`: `"<company>" news <recent>`, `"<company>" funding OR launch OR acquisition`.
- `WebSearch`: `"<person>" "<company>"` for role + public activity.
- LinkedIn / X via `WebSearch` (no login — public results only).
- Trade press for market context.

---

## Output format

```
# Meeting brief — <person / company> (<date>)

**TL;DR:** 2–3 lines — who they are and the one thing to know walking in.

## The person
- Role, tenure, background. Recent public activity worth referencing.

## The company
- What they do, size, business model. Recent news (dated + sourced).

## Likely priorities / pain
- 2–4 bullets, grounded in what you found — not generic guesses.

## Talking points
- 3–5 things to raise that connect to them and to why you're meeting.

## Smart questions to ask
- 3–5 open, specific questions.

## Sources
- [title](url) · [title](url) ...
```

---

## What NOT to do

- Don't fabricate facts, titles, numbers, or quotes. Every claim is sourced or marked `UNVERIFIED`.
- Don't pad. If there's little to verify, say so and keep the brief short — a thin honest brief beats a padded invented one.
- Public sources only. No scraped private data, no guessing personal details.
- Don't bury the lede — the TL;DR should stand on its own.
