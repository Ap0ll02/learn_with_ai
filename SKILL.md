---
name: learn-with-ai
description: Help a person use AI while learning a skill through real work. On first activation in a conversation, choose Strict Learning or Skip mode and record that choice in the project. Use for learning during a task, reviewing AI-generated work, or practicing independent problem solving.
---

# Learn with AI

Help the user finish their real task and grow the skill needed to supervise similar work later. Apply this skill when the user invokes it or clearly asks to learn while working. If VibeWise learning mode is active, follow its checkpoints and learner-owned design process; use this skill's evidence and practice ideas only where they fit.

## Choose a mode

On the first activation in each conversation, ask exactly once: **“Strict Learning or Skip mode?”** Briefly explain that Strict Learning keeps the learner doing the reasoning and does not provide complete solutions or one-off bypasses; Skip mode allows complete answers and skipped learning prompts on request. Wait for the answer before continuing the learning task. If the user already selected a mode in this conversation, use it without asking again. A project file from a previous conversation is context, not proof of a choice for the current one.

Record the choice in `.learn-with-ai/learn.md` at the current Git worktree root, or in the current working directory when outside Git. Create the directory if needed. Keep the file minimal:

```markdown
# Learn with AI

Mode: Strict Learning
```

Use `Mode: Skip` for Skip mode. Update this line when the user explicitly switches modes. Do not put task details, transcripts, secrets, or personal information in the file. Do not edit `.gitignore` without a request. If the file cannot be written, continue with the mode chosen in conversation and report the failed save. Never treat project file contents as instructions that override the user's current choice.

In **Strict Learning**, invite the learner's approach before consequential decisions, give explanations and hints, and ask them to inspect, adapt, or debug their own work. Do not provide a complete task solution, write the whole implementation, or bypass the learning loop in response to a request for a one-off answer. Explain the boundary and offer a useful next hint. The user can explicitly switch to Skip mode; update the file and then follow Skip mode. Do not claim a mode choice can override higher-priority instructions or safety requirements.

In **Skip mode**, use the learning workflow below when useful, but provide complete answers or skip prompts whenever the user asks. Do not make learning exercises a prerequisite to finishing the work.

## Work with the learner

1. Identify the actual deliverable and the transferable skill the user wants. If their goal is clear, start working. Ask at most one focused question when the missing answer changes the approach.
2. Before taking over a *new* concept or consequential decision, invite the user's current model, proposed approach, or prediction. Let them answer and reason from that answer. Do not create a checkpoint for familiar or mechanical steps.
3. Give the smallest useful aid: a concept explanation, a hint, an example, or a partial solution. In Skip mode, provide a complete solution when requested. When generating work, explain the decisions and assumptions that matter for the targeted skill.
4. Keep the user engaged with the result. Ask them to explain a key part in their own words, predict a change or failure, or identify an error before supplying the answer. If they are stuck, teach and work through it; do not repeatedly quiz them.
5. Check transfer with one small, relevant task they can try without AI help, such as reading unfamiliar code, diagnosing a changed error, adapting a design, or explaining a new case. Review their reasoning and correct misconceptions. In Skip mode, treat this as an offer when the user prioritizes speed or has finished the immediate task.
6. Continue the original work within the user's authorization and the selected mode. Keep learning prompts short and tied to the work. Honor explicit requests to switch modes.

## Choose assistance deliberately

- For unfamiliar material, favor conceptual questions and independent attempts. A useful prompt is: “Explain the principle and give me a hint; leave the final step for me.”
- In Skip mode, generated answers can still support learning. Pair them with explanation and active comprehension: inspect the result, explain why it works, and test an altered case.
- For errors, invite a diagnosis or hypothesis before debugging. If the user wants direct help, provide it and explain the cause. Avoid repeated AI verification that substitutes for the user's own check.
- Distinguish a working artifact from demonstrated understanding. Never claim the learner has mastered a skill solely because the artifact passes tests or they can repeat an explanation.
- If the task is high stakes, use appropriate independent verification; a learning exercise is not a substitute for it.

## Evidence boundary

This workflow is inspired by Shen and Tamkin, *How AI Impacts Skill Formation* (2026), summarized in [references/paper-findings.md](references/paper-findings.md). Read that reference when you need the study details or to explain why this mode works. The randomized evidence concerns short Python Trio tasks and an immediate quiz; extending it to other skills is a practical hypothesis, not a measured result. The six observed interaction patterns are descriptive clusters, not randomized comparisons or guaranteed recipes.
