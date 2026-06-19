# Skills For Vibe Engineering

My philosophy: modern development as we knew it is already in the past. The real engineer's job today is to use all their knowledge to build a system of working with AI agents that lets them focus on problems, not on code. The agent already knows and can do a lot — you just need to arm it with the right skills, point it in the right direction, and it will handle all the routine programming work as effectively as the skill's author.

## Quickstart (30-second setup)

1. Install the skills into your agent:

  ```bash
  npx skills@latest add https://github.com/stovberpv/skills
  ```

2. Pick the skills you want and choose which coding agents to install them on.
3. Run `/converge-me` or `/persuade-me` in your agent.

Bam — you're ready to go.

## Why These Skills Exist

These skills are not just prompts. They are engineering artifacts.

They weren't born in a vacuum — they emerged from real observation, study, experimentation, and repeated use in a live codebase alongside an AI agent. Each one is distilled engineering experience, crystallized from hundreds of cycles of “task → solution → review → rework”.

I think of skills as machine instructions for a processor — only the processor here is a language model. Instructions must be precise, atomic, and predictable. A typical prompt is like a high‑level language: expressive, but verbose and open to interpretation. A skill is like assembly: each instruction does exactly one thing, executes fast, and leaves no room for ambiguity.

When you arm your agent with the right skills, you're not just “asking” it to do something — you're giving it a proven, step‑by‑step sequence. This lets you focus on the task, not the code. The agent already knows how to write code. Skills tell it how to think about the problem before writing a single line.

### 1: `converge-me`

The problem. While working on an unfamiliar codebase, I found myself in a context that was new to me but well‑known to the agent. I couldn’t rely on my intuition, and the agent couldn’t grasp my real intent without structure. We needed to quickly synchronise our understanding.

The fix. [converge-me](https://github.com/stovberpv/skills/blob/main/skills/decision/converge-me/SKILL.md) acts as a navigator. It:

- Educates first — establishes a shared vocabulary so you and the agent speak the same language.
- Maps the solution space — lays out 2–4 likely approaches with their core tradeoffs.
- Forces narrowing — asks one question at a time, each one eliminating at least one approach entirely.
- Summarises continuously — after each answer, it tells you what’s been ruled out, what remains, and which decision matters most.

Use it whenever you need to quickly get your bearings in an unfamiliar context and reach a sound decision together with the agent.

### 2: `persuade-me`

The problem. Once changes are made, we need to discuss their correctness. Too often, we (or the agent) start defending what’s written instead of searching for the truth. This leads to mediocre solutions being cemented and missed opportunities for improvement.

The fix. [persuade-me](https://github.com/stovberpv/skills/blob/main/skills/decision/persuade-me/SKILL.md) turns the discussion into a structured hypothesis test. It:

- Explains both sides — first lays out the reasoning behind the current implementation and the reasoning behind your concern.
- Tests assumptions — asks one question at a time, each one either strengthening the current solution or strengthening your objection.
- Converges on truth — after each answer, it explains what conclusions can be drawn and what uncertainty remains.
- Stops when it’s done — continues until the implementation is successfully defended or a better one is found.

Use it whenever you have doubts about existing code and want to constructively arrive at the best possible outcome — not just “win” an argument.

## Reference

- [converge-me](https://github.com/stovberpv/skills/blob/main/skills/decision/converge-me/SKILL.md) — synchronises understanding in an unfamiliar context. Maps approaches, narrows via tradeoffs, leads to an aligned plan.

- [persuade-me](https://github.com/stovberpv/skills/blob/main/skills/decision/persuade-me/SKILL.md) — stress‑tests existing solutions. Probes assumptions, cuts through bias, drives toward truth through structured dialogue.

---

These skills are not instructions for the agent — they are instructions for thinking. They distil engineering experience into repeatable practices, turning the chaos of “just ask the agent” into a controlled decision‑making process.

Vibe Engineering is not about turning your brain off. It's about directing it where it adds the most value: to problems, architecture, strategy. Everything else is done by the agent — armed with the right skills.

Build systems. Don't write code.
