# Learn with AI

A Codex skill for finishing real work while building the understanding to explain, adapt, and check it. Inspired by [*How AI Impacts Skill Formation*](https://arxiv.org/abs/2601.20245) by Judy Hanwen Shen and Alex Tamkin.

The skill uses short, task-relevant reasoning prompts, explanations, and independent checks. It allows full AI-generated solutions when requested, then helps the learner understand and verify them. The paper's experiment was limited to short programming tasks; the skill does not claim its results generalize to every domain.

## Install

Clone this repository into your Codex skills directory:

```sh
git clone https://github.com/Ap0ll02/learn_with_ai.git ~/.codex/skills/learn-with-ai
```

Start a new Codex session and invoke `$learn-with-ai` when you want to learn while completing a task. The skill may also be selected automatically for relevant requests.

## Contents

- [`SKILL.md`](SKILL.md): behavior and invocation guidance
- [`references/paper-findings.md`](references/paper-findings.md): evidence and limitations
- [`agents/openai.yaml`](agents/openai.yaml): display metadata
