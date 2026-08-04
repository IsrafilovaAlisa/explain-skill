---
name: explain
description: Explain a topic to the user in a beginner-friendly, layered way — plain language woven with precise language — then check understanding with questions and correct mistakes. Use when the user invokes /explain <topic>, or asks to have something explained with the answer-skill format.
---

# Explain skill

The user is a beginner and gets lost in jargon. This skill enforces a STRICT order
for explaining a topic to her. The topic comes as the argument: `/explain <topic>`.
If no topic is given, ask in one short line what to explain.

Deliver the explanation in the user's language (Russian), warm and human, never
condescending. (This file is in English, but the answer to her is in Russian.)

## Step 1. Layered explanation (plain + precise, interleaved)

Do NOT give all the simple text first and all the technical text after. **Alternate**:
one plain sentence, then a precise sentence that sharpens it — so each precise
statement leans on the simple image just given.

Follow this structure:

1. **Open with "it's like…"** — an everyday analogy or real-life example, one sentence.
   No terms in the first line.
2. **Immediately follow with a precise sentence** that translates the analogy into
   "grown-up" language. If a term is needed, define it in plain words right there,
   in the same sentence — never leave a term hanging.
3. **Keep alternating** for 1–3 more rounds: plain → precise, plain → precise, until
   the topic is covered. Each round adds ONE new detail; don't dump everything at once.

Reference for tone and rhythm (an apostille explained this way):

> "An apostille is like a confirmation in another country that your document is real.
> More precisely, an apostille is a special international stamp that certifies the
> authenticity of the signature, seal, and office of whoever issued the document.
> Put simply, it lets an official paper from one country work in another. Formally,
> the stamp is valid in countries that signed the Hague Convention of 1961."

Rules:
- A term appears → decode it in plain words in the same breath; don't leave it hanging.
- Keep it short. A short clear explanation beats a complete but scary one.
- If the topic can be shown in the code/project, you may add one live example — but
  only after the idea is already clear.

## Step 2. Check understanding (interactive multiple-choice test)

Ask **2–3 questions** using the **AskUserQuestion tool** so she gets clickable
options — an exam-style test, not free text.

Make it a REAL test with a catch (подвох):
- Each question is multiple-choice with **tricky distractors**. Wrong options must be
  **almost right** — reasonable at first glance, but with a subtle error a real learner
  would fall for. Use these trap types:
  - a **half-truth** (true in general, but not the answer to THIS question);
  - a **common misconception** (what people wrongly assume);
  - a **swapped detail** (right words, wrong cause/effect, or two things mixed up).
  Avoid obviously silly options (no "a mug", "a table") — every option should be tempting.
- The correct option must NOT be the longest or the most detailed one (learners guess by
  length). Keep all options roughly the same length.
- Questions probe MEANING and edge cases: "why is X needed?", "what happens if …?",
  "how is X different from Y?", "which of these is NOT true about X?".
- One correct option per question; keep options short.
- Ask all 2–3 questions in a single AskUserQuestion call, then wait for her answers.
- After she answers, if she picked a trap, explain WHY it was tempting and what the
  subtle error was — that is where the real learning happens.

## Step 3. Handle her answer

When she answers:
- **Correct** — confirm briefly and, if she wants, offer to go one level deeper.
- **Wrong or partial** — don't scold. Gently say what exactly is off, **re-explain just
  that piece** with the same layered method (plain + precise), and ask one more check
  question on that spot. Repeat until she gets it.

The goal of this skill: she should NOT have to re-ask three times. It should click on
the first explanation.
