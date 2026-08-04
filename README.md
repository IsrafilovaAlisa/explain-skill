# explain — a skill that actually makes things click

An agent skill that explains any topic in a **beginner-friendly, layered way** — plain
language woven together with precise language — and then **quizzes you** with an
interactive, exam-style multiple-choice test to make sure it really landed.

Built for people who get lost in jargon: no wall of terms, no "just Google it". Every
term is decoded in the same breath it appears.

## What it does

When you run `/explain <topic>`, the skill:

1. **Explains in layers** — starts with an everyday "it's like…" analogy, then sharpens
   it with a precise sentence, alternating simple → precise so each idea builds on the
   last. One new detail at a time, never a jargon dump.
2. **Tests you** — asks 2–3 interactive multiple-choice questions with *tricky*
   distractors (almost-right traps), so you can't pass by guessing.
3. **Corrects gently** — if you fall for a trap, it explains *why* the wrong answer was
   tempting and re-teaches just that piece.

## Install

Requires an agent that supports skills (Claude Code, Cursor, Codex, and others).

```bash
npx skills add IsrafilovaAlisa/explain-skill
```

Install into a specific agent:

```bash
npx skills add IsrafilovaAlisa/explain-skill -a claude-code
```

Then restart your agent so it picks up the new skill.

## Usage

```
/explain что такое CDN
/explain what is Docker
/explain how DNS works
```

The topic can be anything — a tech concept, a legal term, an everyday idea.
