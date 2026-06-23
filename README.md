# eTop Public Skills

Free, open **Agent Skills** shared by [eTop Technology](https://etoptechnology.com) — turn a generic AI into one that works like an expert in *your* field, in whatever AI tool you already use.

A **Skill** is just one markdown file (`SKILL.md`) that captures how *you* do a repeatable job: the sources you trust, the judgment calls you make, the format you expect back. Save it once and the AI stops guessing like a generalist and starts working like someone you trained. No code required.

> Skills are an **open standard** — the same `SKILL.md` is read by 30+ agents (Claude Code, OpenAI Codex, Cursor, VS Code, Gemini CLI, Windsurf, and more). For project-wide rules, [`AGENTS.md`](https://agents.md) is the cross-tool sibling.

---

## The skills

| Skill | What it does | Try it |
|---|---|---|
| [**news**](skills/news/SKILL.md) | A daily AI/tech brief — the right sources, noise stripped, flagged for what matters, same format every time. | `/news today` |
| [**brand-voice**](skills/brand-voice/SKILL.md) | Drafts or edits any text in *your* house style, so it doesn't read like generic AI. | `/voice edit` |
| [**meeting-prep**](skills/meeting-prep/SKILL.md) | A one-page, sourced brief on whoever you're about to meet. | `/prep Jane Doe at Acme` |

Each one ships with **example content you're meant to replace.** The skill is a template; *your* sources, *your* style guide, *your* angle are what make it expert. Look for the `Customize this skill` callouts.

---

## Install (Claude Code)

Copy any skill folder into your skills directory:

```bash
# user-global (available everywhere)
cp -r skills/news ~/.claude/skills/

# or project-scoped
cp -r skills/news <your-repo>/.claude/skills/
```

Then just type the command — `/news`, `/voice`, `/prep`. That's it.

## Use them in every other tool

Your expertise doesn't change between tools — only *where the file lives* or *which box you paste it into*.

**Drop a file (coding agents read it automatically):**

| Tool | Where it goes |
|---|---|
| Claude Code | `~/.claude/skills/<name>/SKILL.md` |
| OpenAI Codex | `skills/<name>/SKILL.md` · `AGENTS.md` |
| Cursor | `.cursor/rules/*.mdc` (also reads `AGENTS.md`) |
| GitHub Copilot | `.github/copilot-instructions.md` |
| Windsurf · Gemini CLI · Zed · VS Code · +30 | `AGENTS.md` / `SKILL.md` |

**Paste in the UI (no files, same playbook):**

| Tool | Where it goes |
|---|---|
| ChatGPT | New → **Custom GPT** → paste the body into Instructions |
| Google Gemini | New → **Gem** → Role · Style · Knowledge · Format |
| Claude (web / desktop) | Settings → **Capabilities** → upload the Skill |

---

## How to write your own

1. **Pick a job where your judgment beats a generalist's** — a recurring task you'd hate to explain twice.
2. **Write the trigger** — the `description` in the frontmatter. List the phrases that should summon it; that's what the AI matches on.
3. **Write your playbook** — sources, steps, judgment calls, output format. Plain English, the way you'd brief a new hire. Add a "what NOT to do."

The anatomy of every `SKILL.md`:

```markdown
---
name: my-skill
description: One line on WHAT it does and WHEN to fire it (the trigger phrases).
---

# My Skill

## Sources / inputs    ← what you trust
## Process             ← your steps + judgment
## Output format       ← how you want it back
## What NOT to do      ← the guardrails
```

---

## Built by eTop Technology

We're a managed IT and security provider in Redlands, CA. We build AI into how we run our own shop — these skills are a small piece of that, shared freely.

**Want help putting AI to work in your business?** Let's talk.

- 🌐 [etoptechnology.com](https://etoptechnology.com)
- ✉️ [sales@etoptechnology.com](mailto:sales@etoptechnology.com)
- 📞 951-398-0021
- 📍 611 W. Redlands Blvd., Suite G, Redlands, CA 92373

---

## Learn more

- [Anthropic — Equipping agents with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)
- [Claude Code — Skills docs](https://code.claude.com/docs/en/skills)
- [AGENTS.md](https://agents.md) — the cross-tool instruction-file standard

## License

[MIT](LICENSE) — use, fork, and adapt freely. PRs with new starter skills welcome.
