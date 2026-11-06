---
name: english-bug-report
description: Write or translate bug reports into English using a fixed title, Steps, Expected, Actual, and optional concise analysis format. Use when the user asks for an English bug report; do not use for test cases or general code-review findings unless the user wants them formatted as a bug.
---

# English Bug Report

Produce a concise bug report entirely in English. Use facts from the current conversation, linked requirement, PR, test evidence, screenshots, or details supplied by the user.

## Required format

Use exactly this structure:

```markdown
[Module] PR #<number> <brief bug summary>

**Steps**
1. First step
2. Second step

**Expected**
Specific expected behavior.

**Actual**
Specific observed behavior.

Optional concise bug analysis.
```

Apply these rules:

- The title must be one line. Put the functional module inside square brackets, then the PR number, then a brief description of the bug.
- Use the form `PR #<number>` unless the user supplies a different PR-number style.
- Write `**Steps**`, `**Expected**`, and `**Actual**` exactly as shown, each on its own line and in bold.
- Start the content for each section on the following line.
- Number the steps `1.`, `2.`, `3.` when there is more than one step. A single step may be written without a number.
- Leave one blank line before `**Expected**` and one blank line before `**Actual**`.
- When a supported bug analysis is available, leave one blank line after the Actual content and add one concise analysis sentence. Do not add an Analysis heading unless the user explicitly requests one.
- Do not invent a root cause. Omit the analysis when the evidence does not support it.
- Do not add severity, priority, environment, notes, recommendations, attachments, greetings, introductions, conclusions, or any other content.
- Keep steps reproducible and keep Expected and Actual specific and observable.
- Output only the bug report. Do not put it in a code fence.

If the functional module or PR number is genuinely unavailable from the request and conversation, ask for the missing value before drafting. Once the report is drafted, follow the output-only rule.
