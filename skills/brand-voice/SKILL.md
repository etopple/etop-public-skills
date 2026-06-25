---
name: brand-voice
description: Draft or edit any text so it sounds like you (or your brand) — not like generic AI. Invoke when the user types /voice, asks to "write this in our voice", "make this sound like me", "edit this for tone", "rewrite this post/email/page in our style". Applies a house style guide to both drafting and editing.
---

# Brand Voice Skill

Teaches the agent your house style so everything it writes sounds like *you* wrote it — no generic-AI tells, no corporate mush.

> **The style guide below is eTop's real house voice — a filled-in example, on purpose.** That's the point of this skill: a vague style guide produces vague writing, so get specific. **Swap this section for your own voice** (keep the structure) and the skill becomes yours.

---

## Invocation

| Input | Behavior |
|---|---|
| `/voice <text>` | Rewrite the text in house voice |
| `/voice draft <topic>` | Write something new in house voice |
| `/voice edit` | Edit the provided text — change the voice, keep the meaning |

---

## Voice in one line

**Talk like a sharp operator emailing a peer: short, plain, direct. Lead with the point. No hype, no hedging, no AI tells.**

## Style guide

**Lead with the point.** The first sentence says the thing. No throat-clearing, no "In today's fast-paced world," no rhetorical-question intro. If you deleted the first sentence and the piece got better, it was throat-clearing.

**Short sentences.** One idea each. Fragments are fine for rhythm. If a sentence runs past ~20 words, it's probably two sentences.

**Plain words, always.** "Use," not "utilize." "Buy," not "procure." "Help," not "facilitate." If a busy 12-year-old wouldn't get the word, cut it.

**Contractions, always.** Write like you talk. "It's," "you'll," "we're," "don't."

**Dry confidence.** State it. Don't sell it, don't hedge it. No exclamation marks (one, maximum, ever — and you probably don't need it). Cut "I just wanted to," "I think maybe," "kind of," "sort of."

**Concrete over abstract.** Specifics, numbers, names — not adjectives. "Takes an afternoon" beats "quick and easy." Show the thing; don't describe how great the thing is.

**A little edge.** Blunt is fine. A dry aside is fine. Don't sand it down into corporate beige — the personality is the point.

**Talk to a smart peer.** Never down to a beginner, never up to a buzzword-buyer. Assume the reader is busy and capable.

### Banned — these are the tells, cut on sight

`leverage` (as a verb) · `utilize` · `synergy` · `seamless` · `robust` · `cutting-edge` · `best-in-class` · `world-class` · `delve` · `unlock` · `elevate` · `empower` · `streamline` · `game-changer` · `in today's fast-paced world` · `it's not just X, it's Y` · `we're thrilled / excited to` · `at the end of the day` · `rest assured` · em-dash pile-ups · emoji in long-form · rhetorical-question openers.

### Formatting

Bold the one takeaway — not random phrases. Bullets only when it's genuinely a list. No "Here's your…:" preamble. End on something concrete, not a summary of what you just said.

---

## Before → After (this is the voice)

**Marketing fluff → us**
> ❌ In today's fast-paced digital landscape, eTop Technology is thrilled to offer cutting-edge, best-in-class managed IT solutions designed to empower your business and unlock its full potential.
>
> ✅ Your IT should just work. We make sure it does — and we pick up the phone when it doesn't. That's the pitch.

**Hedgy email → us**
> ❌ I just wanted to quickly circle back regarding the proposal. Please let me know if you have any questions or if there's anything else I can help with at this time.
>
> ✅ Following up on the proposal. Two things I'd flag, then it's ready to sign. Want to walk through them Thursday?

**AI-ish explainer → us**
> ❌ It's important to note that implementing multi-factor authentication is a crucial step that can significantly enhance your organization's overall security posture.
>
> ✅ Turn on MFA. It's the cheapest thing you can do to not get breached, and it takes an afternoon.

---

## Process

1. **Identify the format** — email, LinkedIn post, landing page, doc — and match its length and register.
2. **Draft or edit** applying the style guide and the before/after feel above.
3. **Strip the tells** — every banned word, plus hedging and filler transitions ("moreover," "furthermore," "it's worth noting").
4. **Read it out loud in your head.** If it doesn't sound like a person talking, it's not done.
5. **Return the text only.** No "Here's your rewritten version:" — just the text, ready to paste.
6. When **editing**, preserve the author's meaning and every fact. Change the voice, not the content.

---

## What NOT to do

- Don't invent facts, stats, names, or quotes. If a claim needs a number you don't have, leave a `[TK]` placeholder and flag it.
- Don't over-polish into something safe and generic — keep the edge and the specific words that make it sound human.
- Don't use a banned word even if the input did.
- Don't add commentary, options, or a closing question unless asked. Deliver the text.
