# 多平台发布追踪表

一个给创作者、独立团队、内容运营者使用的本地优先发布清单。

你可以把它理解成一个很轻的“内容分发中控台”：左边放内容项目，顶部放平台和账号，发完哪个账号就点一下打勾。它不需要注册、不需要数据库、不需要后端，打开网页就能用，数据保存在你自己的浏览器里。

![多平台发布追踪表预览](assets/screenshots/overview.png)

## 它解决什么问题

很多内容并不是只发一次。

一条选题可能会变成：

- 短视频
- 图文笔记
- 公众号文章
- Newsletter
- 播客
- 博客
- 小课
- 社群内容

真正麻烦的不是“写一条内容”，而是你很快会忘记：

- 哪个平台已经发了？
- 哪个账号还没发？
- 哪条内容需要补一个短视频版本？
- 哪篇文章已经同步到 Newsletter？
- 哪些内容值得 24 小时、48 小时、7 天后复盘？

这个表格就是为了解决这件事：把多平台发布状态变成一张一眼能看懂的表。

## 适合谁

你会适合用它，如果你：

- 一个内容要分发到多个平台
- 同时运营多个账号
- 经常把长内容拆成短视频、图文、文章、播客或课程
- 不想上复杂的项目管理工具
- 想要一个本地保存、可导出 CSV 的轻量表格
- 希望团队或 AI Agent 都能围绕同一张发布表工作

## 核心逻辑

这张表只有三个核心概念：

- 行：内容项目、选题、合作项目、发布任务
- 列：平台、账号、栏目
- 勾选：这个内容已经发到这个账号

比如你有一条内容叫 `Short tutorial: how the tracker works`，它可能已经发到了短视频账号、博客账号，还没发 Newsletter。你只需要在对应格子里打勾，就能看到完整状态。

## 主要功能

- 点击格子即可打勾，标记已发布
- 顶部账号名称可以直接编辑
- 可以新增平台和账号列
- 可以删除不需要的账号列
- 每条内容可以添加数据备注
- 数据备注支持红、黄、绿三种状态颜色
- 按月份分组，月份可以收起或展开
- 支持 CSV 导出和导入
- 数据保存在浏览器 Local Storage

## 一分钟上手

### 方式一：直接打开

下载仓库后，直接打开：

```bash
open index.html
```

### 方式二：用本地服务打开

```bash
python3 -m http.server 8765
```

然后访问：

```text
http://127.0.0.1:8765/
```

## 怎么改成你自己的表

1. 点击 `Platform +`，增加你的平台或账号。
2. 点击顶部账号名称，直接改成你自己的账号名。
3. 点击 `Add content`，增加一条内容项目。
4. 发完某个平台后，点击对应格子打勾。
5. 用 `Export CSV` 定期备份，或者导入到表格软件里继续分析。

## 使用场景示例

### 内容创作者

把一个选题拆成小红书、Newsletter、视频、播客、博客、小课等不同版本，逐个平台打勾，避免漏发。

### 独立产品团队

把一次产品更新同步到官网、邮件列表、社交账号、社区、教程、发布帖，每个渠道一个格子。

### AI Agent 工作流

让 AI 先生成一组发布任务，再导入 CSV。你只需要在表格里检查、改名、打勾和复盘。

### 商务合作排期

把每个合作项目放在左侧，右侧用账号列追踪脚本、初稿、发布、投流、返点等状态。

## 数据隐私

这个项目默认不连接任何服务器。

你的内容保存在浏览器的 Local Storage 里，不会自动上传到任何地方。如果你清理浏览器数据，Local Storage 可能会被删除，所以建议定期导出 CSV 做备份。

## 截图

### 总览

![Overview](assets/screenshots/overview.png)

### 直接编辑账号名

![Edit account names](assets/screenshots/edit-accounts.png)

### 新增或删除账号列

![Account management](assets/screenshots/account-management.png)

## AI Skill

仓库里有一份配套的 `SKILL.md`。

中文名：**内容分发中控表**。

它不是给普通用户看的说明书，而是给 AI Agent 使用的工作流说明：当你把一堆内容想法、平台账号、发布状态、接广排期或复盘要求交给 AI 时，AI 可以按照这份 Skill，把信息整理成适合这张表使用的行、列、状态、CSV 和复盘提醒。

## 文件结构

- `index.html`：完整网页应用
- `SKILL.md`：AI Agent 使用的 Skill 文档
- `REDDIT_POST.md`：Reddit 发布文案草稿
- `assets/screenshots/`：干净演示截图

## License

MIT

---

# Multi-platform Publishing Tracker

A simple local-first publishing checklist for creators, indie teams, and content operators who repurpose one idea across many platforms.

It is a single-page web app. No signup, no database, no backend required. Open it in a browser and your data is saved in Local Storage.

![Tracker overview](assets/screenshots/overview.png)

## Search Keywords

English keywords:

`multi platform publishing`, `content publishing tracker`,
`social media publishing checklist`, `creator content calendar`,
`content distribution workflow`, `publishing status tracker`,
`repurpose content across platforms`, `newsletter publishing checklist`,
`podcast content distribution`, `local-first content tracker`.

中文关键词：

`多平台发布`, `内容发布追踪`, `发布状态表`, `创作者发布清单`,
`自媒体内容分发`, `多账号发布`, `发布日历`, `内容复盘提醒`,
`内容运营工具`, `创作者工具`.

## What It Does

- Track one content idea across multiple platforms and accounts.
- Click cells to mark where a piece has already been published.
- Edit platform account names directly in the table header.
- Add or delete platform/account columns.
- Add notes or performance labels to each content row.
- Collapse months to focus on recent work.
- Export and import CSV files.

## Why This Exists

Most content teams do not need a complex project management system for distribution. They need a visible grid:

- rows = content ideas or projects
- columns = platforms and accounts
- checkmarks = already published

This project is intentionally small so people can adapt it to their own workflow.

## Who It Is For

Use this tracker if you:

- publish one idea across multiple platforms
- run several social accounts at the same time
- turn podcast episodes into clips, notes, articles, and posts
- need a visible checklist instead of a heavy project-management tool
- want a local-first tracker that can be backed up with CSV

## Quick Start

Option 1: open directly

```bash
open index.html
```

Option 2: run a local server

```bash
python3 -m http.server 8765
```

Then open:

```text
http://127.0.0.1:8765/
```

## How To Customize

1. Click `Platform +` to add your own platform group and account.
2. Click any account name in the table header to rename it.
3. Click `Add content` to add a new content idea.
4. Click a cell when that content has been published to that account.
5. Use `Export CSV` for backup or spreadsheet editing.

## Privacy

The app stores data in your browser's Local Storage. It does not send your content anywhere.

If you clear browser data, Local Storage may be removed. Export a CSV backup if the tracker matters to you.

## Screenshots

### Overview

![Overview](assets/screenshots/overview.png)

### Editing Account Names

![Edit account names](assets/screenshots/edit-accounts.png)

### Add or Delete Accounts

![Account management](assets/screenshots/account-management.png)

## Files

- `index.html` - the full app
- `SKILL.md` - companion AI Agent workflow
- `REDDIT_POST.md` - suggested Reddit post copy
- `assets/screenshots/` - clean demo screenshots

## License

MIT
