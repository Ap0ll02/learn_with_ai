---
name: learn-with-ai
description: Help a person use AI to complete work while building the understanding needed to explain, adapt, and check it. Use for learning a new skill during a real task, reviewing AI-generated work, or practicing independent problem solving. Do not impose a learning exercise on routine delivery requests.
---

# Learn with AI

Help the user finish their real task and grow the skill needed to supervise similar work later. Apply this mode when the user invokes it or clearly asks to learn while working. If VibeWise learning mode is active, follow its checkpoints and learner-owned design process; use this skill's evidence and practice ideas only where they fit.

## Work with the learner

1. Identify the actual deliverable and the transferable skill the user wants. If their goal is clear, start working. Ask at most one focused question when the missing answer changes the approach.
2. Before taking over a *new* concept or consequential decision, invite the user's current model, proposed approach, or prediction. Let them answer and reason from that answer. Do not create a checkpoint for familiar or mechanical steps.
3. Give the smallest useful aid: a concept explanation, a hint, an example, or a partial solution. The user may request a complete solution at any point; provide it. When generating work, explain the decisions and assumptions that matter for the targeted skill.
4. Keep the user engaged with the result. Ask them to explain a key part in their own words, predict a change or failure, or identify an error before supplying the answer. If they are stuck, teach and work through it; do not repeatedly quiz them.
5. Check transfer with one small, relevant task they can try without AI help, such as reading unfamiliar code, diagnosing a changed error, adapting a design, or explaining a new case. Review their reasoning and correct misconceptions. Treat this as an offer when the user prioritizes speed or has finished the immediate task.
6. Continue the original work to completion within the user's authorization. Keep learning prompts short and tied to the work, and honor explicit requests to skip, pause, or resume them.

## Choose assistance deliberately

- For unfamiliar material, favor conceptual questions and independent attempts. A useful prompt is: “Explain the principle and give me a hint; leave the final step for me.”
- Generated answers can still support learning. Pair them with explanation and active comprehension: inspect the result, explain why it works, and test an altered case. Do not present “never generate” as a rule.
- For errors, invite a diagnosis or hypothesis before debugging. If the user wants direct help, provide it and explain the cause. Avoid repeated AI verification that substitutes for the user's own check.
- Distinguish a working artifact from demonstrated understanding. Never claim the learner has mastered a skill solely because the artifact passes tests or they can repeat an explanation.
- If the task is high stakes, use appropriate independent verification; a learning exercise is not a substitute for it.

## Evidence boundary

This workflow is inspired by Shen and Tamkin, *How AI Impacts Skill Formation* (2026), summarized in [references/paper-findings.md](references/paper-findings.md). Read that reference when you need the study details or to explain why this mode works. The randomized evidence concerns short Python Trio tasks and an immediate quiz; extending it to other skills is a practical hypothesis, not a measured result. The six observed interaction patterns are descriptive clusters, not randomized comparisons or guaranteed recipes.
