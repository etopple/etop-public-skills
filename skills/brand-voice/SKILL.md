---
name: brand-voice
description: Draft or edit any text so it sounds like you (or your brand) — not like generic AI. Invoke when the user types /voice, asks to "write this in our voice", "make this sound like me", "edit this for tone", "rewrite this post/email/page in our style". Applies a house style guide to both drafting and editing.
---

# Brand Voice Skill

Teaches the agent your house style so everything it writes sounds like *you* wrote it — no generic-AI tells, no corporate mush.

> **Customize this skill — this is the whole point.** Replace the STYLE GUIDE below with your own rules. The template ships with examples; swap them for the real ones. The more specific and opinionated, the better the output. A vague style guide produces vague writing.

---

## Invocation

| Input | Behavior |
|---|---|
| `/voice <text>` | Rewrite the text in house voice |
| `/voice draft <topic>` | Write something new in house voice |
| `/voice edit` | Edit the provided text — change the voice, keep the meaning |

---

## Style guide  (EDIT ME — these are examples)

**Tone:** confident, plain-spoken, a little dry. Talk to a smart peer — never down to a beginner.

**Sentences:** mostly short. One idea each. Vary the rhythm so it doesn't read like a list.

**Person:** first person plural ("we"); address the reader directly as "you".

**Words we like:** concrete nouns, strong verbs, specifics over adjectives.

**Words we ban:** *leverage* (as a verb), *synergy*, *seamless*, *robust*, *delve*, *unlock*, *in today's fast-paced world*, *it's not just X — it's Y*, *game-changer*. No exclamation marks in long-form.

**Formatting:** bold the one takeaway, not random phrases. No emoji in long-form (a single one is fine to close a social post). Bullets only when the content is genuinely a list.

**Structure:** lead with the point. No throat-clearing intro, no "in this post we'll explore." End on something concrete, not a summary of what you just said.

---

## Process

1. **Identify the format** — email, LinkedIn post, landing page, doc — and match its length and register.
2. **Draft or edit** applying the style guide above.
3. **Strip the AI tells** — the banned words, hedging, and filler transitions ("moreover", "furthermore", "it's worth noting").
4. **Return the text only.** No preamble like "Here's your rewritten version:" — just the text, ready to paste.
5. When **editing**, preserve the author's meaning and every fact. Change the voice, not the content.

---

## What NOT to do

- Don't invent facts, stats, names, or quotes. If a claim needs a number you don't have, leave a `[TK]` placeholder and flag it.
- Don't over-polish into something safe and generic — keep the edges and the specific words that make it sound human.
- Don't use a banned word even if the input did.
- Don't add commentary, options, or a closing question unless asked. Deliver the text.
