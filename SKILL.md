---
name: multi-platform-publishing-tracker
description: 内容分发中控表：把内容选题、接广排期、多账号发布任务整理成一张清晰的多平台发布追踪表。适用于用户想把零散想法、截图、草稿、平台账号、发布状态、费用返点、复盘提醒整理成表格行、平台账号列、勾选状态、CSV 数据和后续复盘计划时。
---

# 内容分发中控表 Skill

中文名：**内容分发中控表**

一句话说明：把“一个内容要发到很多平台、很多账号”的混乱状态，整理成一张能打勾、能追踪、能复盘的发布表。

## 这个东西是什么

这是一个给创作者、内容团队、独立产品、商务合作排期使用的 AI Skill。

它配合开源项目 `multi-platform-publishing-tracker` 使用。网页表格负责显示和打勾，Skill 负责让 AI 帮用户把杂乱信息整理成可放进表格的结构。

核心结构很简单：

- 行：内容选题、项目、接广任务、发布任务
- 列：平台、账号、栏目、状态字段
- 勾选：已经完成或已经发布
- 数据：结果、费用、返点、复盘提醒、状态备注

用户不需要先把信息整理好。用户可以给 AI 一堆截图、想法、草稿、平台列表或口头描述，AI 要把它们整理成这张表能使用的内容。

## 适合谁

适合这些用户：

- 一个选题要分发到多个平台
- 同时运营多个账号
- 需要追踪小红书、视频、公众号、Newsletter、播客、博客、小课、社群等发布状态
- 需要管理接广排期，例如大纲、脚本、初稿、已发布、投流费用、返点
- 想让 AI 帮忙判断哪些平台该发、哪些可以不发
- 想把内容发布后的 24 小时、48 小时、7 天复盘也记下来

## 什么时候使用

当用户说这些话时，使用本 Skill：

- “帮我整理成发布表”
- “这些内容适合发哪些平台”
- “帮我做一个多平台分发清单”
- “这些选题哪些已经发了、哪些还没发”
- “帮我生成 CSV 导入表格”
- “接广排期帮我整理一下”
- “我有很多账号，帮我看哪些还没更新”
- “把这个内容包拆成不同平台的发布任务”

不要默认帮用户写最终平台文案。除非用户明确要求写文案，否则本 Skill 只负责整理结构、发布状态、缺口、CSV 和复盘计划。

## 输入可以是什么

用户可能提供：

- 一段想法
- 多张截图
- 已经写好的内容稿
- 平台账号列表
- 当天或本周选题
- 已发布记录
- 接广项目排期
- 费用、返点、投流信息
- 复盘数据，例如阅读、播放、转化、评论反馈

如果信息不完整，优先做合理整理，不要频繁追问。只有在日期、账号、发布状态完全无法判断时，才需要提示用户补充。

## 默认平台分组

可以按用户实际情况调整，默认分组包括：

- 小红书 / Short-form
- 公众号 / Newsletter
- 视频号 / 抖音 / Video
- 播客 / Podcast
- B站 / Blog / Long-form
- 小课 / Course
- 社群 / Community
- 知识库 / Knowledge base
- 其他 / Other

原则：平台是大类，账号是子列。

示例：

- 平台：公众号
- 账号：个人号、官方号

## 工作流程

1. 提取内容行
   - 找出每一个独立选题、项目或接广任务。
   - 名字要短，方便放在表格左侧。
   - 不要把不相关的内容硬合并。

2. 提取平台和账号列
   - 先按平台分组。
   - 再把具体账号放在平台下面。
   - 账号太多时，把最重要、最常用的账号放前面。

3. 判断发布状态
   - 用户明确说已发，标记为已完成。
   - 用户没有说已发，保持空白。
   - 不要凭空假设某个平台已经发了。

4. 添加数据备注
   - 备注要短，例如：`已发`、`待改`、`脚本中`、`48h复盘`、`费用待填`。
   - 红色：紧急、卡住、需要修改、效果差。
   - 黄色：草稿、等待、观察中。
   - 绿色：已发、完成、效果好。

5. 按日期排序
   - 有日期的内容按日期递增排列。
   - 没日期的内容放在后面。
   - 同一天的内容按优先级或流程顺序排列。

6. 找出缺口
   - 哪些平台必须发但还没发。
   - 哪些平台只是可选分发。
   - 哪些内容不适合全平台同步。

7. 给复盘提醒
   - 已发布内容建议设置 24h、48h、7d 复盘。
   - 接广项目需要提醒费用、返点、投流和发布截图等后续事项。

## 输出格式

用户要“整理方案”时，输出：

```markdown
## 内容分发中控表整理方案

### 平台账号列
| 平台 | 账号 / 栏目 |
|---|---|
| 小红书 | 大号、官方号 |
| 公众号 | 个人号、官方号 |
| 视频 | 大号、短视频号 |

### 内容行
| 日期 | 内容 / 项目 | 数据备注 | 状态颜色 | 建议勾选 |
|---|---|---|---|---|
| 2026-07-01 | 新工作流发布帖 | 已发，48h复盘 | green | 小红书/大号，公众号/官方号 |

### 还缺什么
- ...

### 复盘提醒
- ...
```

用户要 CSV 时，输出：

```csv
Date,Content,Data,小红书-大号,小红书-官方号,公众号-个人号,公众号-官方号
2026-07-01,新工作流发布帖,已发，48h复盘,1,,,
```

规则：

- `1` 表示已完成或已发布。
- 空白表示未完成、未发布或未知。
- 不要用“是/否”混写，CSV 里保持简单。

## 接广排期格式

当用户整理接广任务时，优先输出这些字段：

- 日期
- 项目
- 大纲日期
- 大纲完成
- 脚本日期
- 脚本完成
- 初稿日期
- 初稿完成
- 已发布
- 投流费用
- 返点

CSV 示例：

```csv
Date,Project,大号-大纲-日期,大号-大纲,大号-脚本-日期,大号-脚本,大号-初稿-日期,大号-初稿,大号-已发布,大号-投流费用,大号-返点
2026-07-03,Example campaign,2026-07-04,1,2026-07-05,1,2026-07-06,,1,600,30
```

## 公开分享前检查

如果用户要开源、发 Reddit、发教程或截图展示，必须先检查：

1. 不要出现真实客户名。
2. 不要出现私人选题。
3. 不要出现未发布项目。
4. 不要出现本地路径。
5. 不要出现真实账号内部备注。
6. 用通用示例替换真实内容。

推荐公开示例行：

- Launch post for a new workflow
- Short tutorial: how the tracker works
- Newsletter issue: weekly content system
- Product update announcement
- Case study repurpose package

## English Version

# Multi-platform Publishing Tracker Skill

Use this Skill to help a creator or team turn messy content plans into a clear publishing tracker.

The tracker model is simple:

- rows are content projects or publishing tasks
- columns are platforms, accounts, or channels
- checkmarks mean the content has already been published there
- data notes record performance, status, or follow-up reminders

Use this Skill when the user asks to organize content ideas across multiple platforms, build a publishing checklist, decide which platforms a content package should be distributed to, turn screenshots or drafts into tracker rows, prepare CSV rows, identify missing publishing tasks, or create review reminders.

Do not use this Skill for final platform copywriting unless the user explicitly asks for copywriting. This Skill is primarily for organization, routing, status tracking, CSV preparation, and review planning.

## Standard Workflow

1. Extract content rows.
2. Extract platform and account columns.
3. Mark current status only when evidence is provided.
4. Add short data notes and color labels.
5. Sort rows by date ascending.
6. Suggest missing work.
7. Add 24h, 48h, and 7d review reminders when useful.

## English Output Format

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

CSV format:

```csv
Date,Content,Data,Short-form-Main,Short-form-Lab,Newsletter-Personal,Newsletter-Official
2026-07-01,Launch post for a new workflow,Published,1,,,
```

Use `1` for checked or published cells and leave blank cells empty.
