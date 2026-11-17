# Learn with AI

A Codex skill for finishing real work while building the understanding to explain, adapt, and check it. Inspired by [*How AI Impacts Skill Formation*](https://arxiv.org/abs/2601.20245) by Judy Hanwen Shen and Alex Tamkin.

On first activation in each conversation, the skill asks you to choose **Strict Learning** or **Skip mode**. Strict Learning keeps you doing the reasoning and does not provide complete solutions or one-off bypasses. Skip mode lets you request full answers or skip learning prompts. You can explicitly switch modes at any time.

The choice is saved in `.learn-with-ai/learn.md` at the project's Git worktree root (or the current directory outside Git). This file contains only the mode. A new conversation asks again, even when a previous choice is saved. If you do not want this local preference tracked in your project repository, add `.learn-with-ai/` to that project's `.gitignore`.

The paper's experiment was limited to short programming tasks; the skill does not claim its results generalize to every domain.

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
- [`LICENSE`](LICENSE): MIT license
