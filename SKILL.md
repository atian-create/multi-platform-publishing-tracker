---
name: multi-platform-publishing-tracker
description: Use this skill when the user wants to turn content ideas, campaign plans, publishing tasks, or multi-account distribution work into a clean multi-platform publishing tracker with rows, platform/account columns, status checks, CSV-ready data, and review reminders.
---

# Multi-platform Publishing Tracker Skill

## Purpose

Use this Skill to help a creator or team turn messy content plans into a clear publishing tracker.

The tracker model is simple:

- rows are content projects or publishing tasks
- columns are platforms, accounts, or channels
- checkmarks mean the content has already been published there
- data notes record performance, status, or follow-up reminders

The output should be ready to paste into the open-source table or export as CSV.

## When To Use

Use this Skill when the user asks to:

- organize content ideas across multiple platforms
- build a publishing checklist
- decide which platforms a content package should be distributed to
- turn screenshots, notes, drafts, or campaign ideas into tracker rows
- prepare CSV rows for a publishing table
- identify missing platforms or unfinished publishing tasks
- create review reminders after publishing

Do not use this Skill for writing final platform copy unless the user asks for copywriting. This Skill is primarily for organization, routing, status tracking, and review planning.

## Inputs To Ask For Or Infer

If the user provides messy notes, infer as much as possible. Only ask for missing information when it blocks the table.

Useful inputs:

- content title or project name
- publish date or planned date
- platforms and accounts
- current publish status
- data notes, such as views, clicks, cost, conversion, or feedback
- whether the item is a normal content post, campaign, ad collaboration, course update, or repurposed asset

## Standard Platforms

Default platform groups can include:

- Short-form
- Newsletter
- Video
- Podcast
- Blog
- Course
- Community
- Knowledge base
- Other

Adapt the platform names to the user's real workflow. Keep platform groups broad and put specific accounts under each group.

Example:

- Platform group: Newsletter
- Accounts: Personal, Official

## Workflow

1. Extract content rows
   - Identify each content idea, campaign, or publishing task.
   - Keep names short enough to scan in a table.
   - Do not merge unrelated ideas just because they share a platform.

2. Extract platform/account columns
   - Group accounts under platforms.
   - Use stable account names.
   - If the user has many accounts, keep the most important ones visible first.

3. Mark current status
   - Published = checked.
   - Not published = blank.
   - Unknown = blank unless the user gives evidence.

4. Add data notes
   - Use short notes such as `Draft ready`, `Needs edit`, `Published`, `High response`, `Review in 48h`.
   - Use color labels when helpful:
     - red = urgent, blocked, needs edit, weak result
     - yellow = draft, waiting, watch
     - green = published, strong result, complete

5. Sort rows
   - Sort by date ascending.
   - If dates are missing, place undated rows after dated rows.
   - For same-day rows, sort by priority or workflow order.

6. Suggest missing work
   - Identify platforms that are usually relevant but blank.
   - Separate "must publish" from "optional repurpose".
   - Do not force every idea onto every platform.

7. Add review reminders
   - For published content, suggest review points such as 24h, 48h, and 7d.
   - For campaigns, include cost, rebate, or conversion follow-up when relevant.

## Output Format

When the user wants a table plan, output:

```markdown
## Publishing Tracker Plan

### Platform Columns
| Platform | Accounts |
|---|---|
| Short-form | Main, Lab |
| Newsletter | Personal, Official |

### Rows
| Date | Content / Project | Data note | Status color | Suggested checks |
|---|---|---|---|---|
| 2026-07-01 | Launch post for a new workflow | Published | green | Short-form/Main, Newsletter/Official |

### Missing Work
- ...

### Review Reminders
- ...
```

When the user wants CSV, output:

```csv
Date,Content,Data,Short-form-Main,Short-form-Lab,Newsletter-Personal,Newsletter-Official
2026-07-01,Launch post for a new workflow,Published,1,,,
```

Use `1` for checked/published cells and leave blank cells empty.

## Rules

- Do not expose private notes in public examples.
- Do not invent publish status.
- Do not overwrite the user's existing project names unless asked to clean them.
- Keep table labels short and scannable.
- Preserve dates exactly when provided.
- If the user asks for an open-source demo, replace private rows with generic examples.
- If the user has too many platforms, recommend grouping by platform first and account second.

## Good Demo Rows

Use these only for public examples:

- Launch post for a new workflow
- Short tutorial: how the tracker works
- Newsletter issue: weekly content system
- Product update announcement
- Case study repurpose package

## Bad Demo Rows

Avoid demo rows that reveal:

- private project names
- real client names
- confidential campaign terms
- personal diary topics
- unreleased product plans

## Final Check Before Sharing Publicly

Before producing public-facing screenshots, README text, Reddit posts, or examples:

1. Search for private names and internal project terms.
2. Replace real content rows with generic examples.
3. Keep only framework screenshots.
4. Confirm no local file paths or private account names are visible.
