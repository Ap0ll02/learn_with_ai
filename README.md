# Learn with AI

A Codex skill for developers who value proficiency and ownership while using AI. It defaults to mentorship: concepts, progressive hints, and read-only review. You can ask for collaboration, delegated chores, or a complete solution whenever you want.

## Install on Linux with Fish

Clone into Codex's user skills directory, then start a new Codex session:

```fish
mkdir -p ~/.codex/skills
git clone https://github.com/Ap0ll02/learn_with_ai.git ~/.codex/skills/learn-with-ai
```

If you already installed it, update it with:

```fish
git -C ~/.codex/skills/learn-with-ai pull
```

The directory name and the `name` in `SKILL.md` are both `learn-with-ai`. Invoke it with `$learn-with-ai`, or ask to learn while coding. Codex can also select it for a relevant request. To use the repository policy in another project, copy [`AGENTS.md`](AGENTS.md) to that project's root and adapt it to your preferences. Installing the skill alone does not copy that policy into other projects.

## Try it

- “Use `$learn-with-ai`. Explain this API and give me one hint for the next step.”
- “Review my diff for correctness and learning gaps. Keep it read-only.”
- “I have a hypothesis about this failure. Help me test it before showing a fix.”
- “Implement this part for me, then explain the decisions I should understand.”

The last request authorizes implementation. Requests to explain, plan, or review do not authorize source edits.

## Why this approach

Shen and Tamkin's [*How AI Impacts Skill Formation*](https://arxiv.org/abs/2601.20245) found that, in a randomized study of short tasks with an unfamiliar Python library, AI-assisted participants scored lower on an immediate knowledge quiz without a statistically significant average completion-time gain. Their observed AI-use patterns suggest that active reasoning matters, but the patterns were descriptive, not randomized treatments. The mentorship workflow here is a practical design choice, not a tested intervention. See [`references/paper-findings.md`](references/paper-findings.md) for details and limits.

## Files

- [`SKILL.md`](SKILL.md): reusable skill instructions
- [`AGENTS.md`](AGENTS.md): repository policy for AI-assisted work
- [`references/paper-findings.md`](references/paper-findings.md): study summary and evidence limits
- [`agents/openai.yaml`](agents/openai.yaml): Codex display metadata
- [`LICENSE`](LICENSE): MIT license
