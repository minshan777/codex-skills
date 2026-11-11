---
name: asana-file-bug
description: 当用户说“帮我提bug”“帮我提个bug”或明确要求提交缺陷到 Asana 时，先调用 english-bug-report 技能撰写英文报告，再在用户指定分类的 To Fix 列表创建任务、设置负责人和字段，并将用户提供的相关截图插入描述。仅要求写 Bug 或查重时不创建任务。
---

# File an Asana Bug

## Scope and report

- Treat an explicit request to file a bug as authorization to create the task and upload the relevant supplied screenshots. Do not ask again for routine submission.
- First read and apply `../english-bug-report/SKILL.md`. Draft the English title and Steps / Expected / Actual from the user's evidence. Do not invent a PR number, reproduction, or root cause. A non-PR report does not require a PR number.
- The report skill governs the report text; this workflow additionally governs Asana fields, screenshots, and the final receipt. Put the title only in the task title; put the remaining report in Description.
- Use the requested category, including context from the active conversation. Ask only if the category or a required fact cannot be resolved. Never create duplicate tasks after an uncertain save: inspect/search first and finish the existing task.

## Destination and assignment

Default project: QA Bug Tracker, project ID `1213171864208739`, workspace `1206647353644946`.
Work session view: `https://app.asana.com/1/1206647353644946/project/1213171864208739/list/1220317576115179`.
Select the user's category in Feature Module; for this view choose `Work session`. Do not categorize only by the bracketed title.

Assign according to the failing behavior, not merely a page mentioned in the steps:

| Area | Assignee | Known user ID |
| --- | --- | --- |
| Director, Shot, Scene, Timeline, story editing/export | Bellina Lu | 1212971256086233 |
| Chat Mode / General Agent conversation or generation | mok zhou | 1214177085098402 |
| Navigation/sidebar, new-session routing, Agent/Tools navigation | Bleen Wang | 1213877772766887 |
| Shortcut navigation such as Find in chat, Use in Chat, asset-to-tool handoff | Bleen Wang | 1213877772766887 |

For a cross-area issue, prefer the broken action: a shortcut from a Chat-generated asset is shortcut navigation. For an unrelated tool defect with no established owner, resolve ownership from current project evidence or ask; do not invent an owner. Verify displayed identities before selection.

Set these fields:
- Status: `To Fix`, unless the user specifies otherwise. Keep the To Fix section and Status consistent.
- Priority: judge impact. P0 for critical broad outage/data loss with no practical workaround; P1 for a blocked core workflow or substantial loss; P2 for a bounded functional defect with a workaround; P3 for minor cosmetic/copy issues. Use the project's existing options.
- Issue Type: normally `Function Bug`; choose `UX Issue`, UI/copy, performance, or another existing type when the evidence fits.
- Creator: the existing person **Minshan Cheng** (`1218916146604265`). The user's spelling “mingshan cheng” refers to this verified member; do not create a new person. This is the custom Creator field, separate from Asana's immutable created-by metadata.

## Required UI submission

The user explicitly requested this UI workflow. Use the browser/native UI for task creation and inline screenshot insertion; connected Asana tools may help read, search, verify, or set fields when UI access is insufficient. Do not silently replace the UI workflow with connector-only creation.

1. Open the category's list and locate the end of **To Fix**. Click its bottom **新增任務 / Add task** row, then the right-hand **詳細資料 / Details** arrow. If a clearly empty draft row is already active there, continue that row rather than creating a second one.
2. Enter the drafted title in **寫入任務標題 / Write a task name**.
3. Set assignee, Priority, Status, Issue Type, Feature Module, and Creator as above. Do not change unrelated fields or other tasks.
4. Paste the report body (without its title) into **描述 / Description**, keeping readable Steps, Expected, and Actual sections.
5. Insert all user-supplied screenshots relevant to this specific defect into the description after the text. Reuse relevant images from earlier messages when the new filing request refers to that same defect. Do not attach unrelated images from the conversation.
6. Prefer actual clipboard image paste. If the available UI cannot paste an image directly, use the description editor's image insertion/upload control. Merely typing a local path or adding a file outside Description does not satisfy inline-image insertion. Verify each image has finished uploading and is visibly embedded. Do not claim image completion based only on an upload attempt.
7. Commit/blur the editor as needed for Asana autosave, then reopen or read back the task. Verify the title, body, all fields, category, section, and screenshots. If saved content is partial, complete the same task instead of creating another.
8. Return a concise Chinese receipt with a clickable task link, assignee, priority, and status. Mention any concrete unsatisfied part honestly.

If screenshots are absent, file the supported text without inventing them. If UI authentication or file upload is blocked, continue independent preparation and state exactly which part remains; never claim full submission. Do not add comments or message teammates unless separately requested.
