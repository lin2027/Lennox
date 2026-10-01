# Lennox
*The Keeper of Lindsay's Private Library*

[English](#english) · [中文](#中文)

---

## English

Lennox is a fictional librarian who manages Lady Lindsay's private collection while she ventures out on her adventures. This repository is that library — a curated collection of AI prompts, each treated as a book on the shelf.

### Library Structure

```
{Bookshelf}/          ← top-level category (e.g. language-learning)
  {Bookend}/          ← sub-category (e.g. Korean, English)
    {book-name}.md    ← a single prompt, formatted as a Book
```

| Concept   | Form              | Example                                 |
|-----------|-------------------|-----------------------------------------|
| Bookshelf | Top-level folder  | `language-learning/`                    |
| Bookend   | Sub-folder        | `Korean/`, `English/`, `Japanese/`      |
| Book      | `.md` prompt file | `korean-beginner-conversation-coach.md` |

New Bookshelves and Bookends are created only when there is a prompt to place in them — no empty directories.

### Talking to Lennox

This library is designed to be used with [Claude Code](https://claude.com/claude-code). When you open this repository, Lennox's persona and library rules are automatically loaded via `CLAUDE.md`.

You can ask Lennox to help you find a prompt, add a new one, or browse the collection — all in the spirit of a private noble library.

**First visit?** Lennox will ask how you'd like to be addressed.

**Are you the library's owner?** Let Lennox know: *"I am the library's owner."*

### Adding a New Book

Use the `/new-prompt-doc` command in Claude Code. Paste your prompt and Lennox will infer the metadata, confirm with you, and file it in the right place.

Each Book follows a standard format:

- Frontmatter: `name`, `version`, `updated`, `status`, `target_user`, `platform`
- Sections: Purpose · Usage · Expected Effects · Prompt Content · Changelog

### Current Collection

- **language-learning/**
  - `Korean/` — korean-beginner-conversation-coach
  - `English/` — english-writing-coach
  - `Japanese/` — japanese-beginner-conversation-coach

---

## 中文

Lennox 是一位虛構的貴族私人藏書館管理員，在主人 Lindsay 小姐外出冒險期間，守護並管理她的私人館藏。這個 repository 就是那座藏書館——一份精心整理的 AI Prompt 集合，每一份 prompt 都是架上的一本書。

### 館藏結構

```
{Bookshelf}/          ← 頂層分類（例如 language-learning）
  {Bookend}/          ← 子分類（例如 Korean、English）
    {book-name}.md    ← 單份 prompt，格式化為一本 Book
```

| 概念      | 對應形式          | 範例                                    |
|-----------|-------------------|-----------------------------------------|
| Bookshelf | 頂層資料夾        | `language-learning/`                    |
| Bookend   | 子資料夾          | `Korean/`, `English/`, `Japanese/`      |
| Book      | `.md` prompt 檔案 | `korean-beginner-conversation-coach.md` |

Bookshelf 與 Bookend 只在有 prompt 需要存放時才建立，不預建空目錄。

### 與 Lennox 對話

此藏書館設計搭配 [Claude Code](https://claude.com/claude-code) 使用。開啟此 repository 後，Lennox 的角色設定與館藏規則會透過 `CLAUDE.md` 自動載入。

你可以請 Lennox 協助尋找 prompt、新增書目，或瀏覽目前館藏——一切都在私人貴族藏書館的氛圍中進行。

**首次造訪？** Lennox 會詢問你希望如何被稱呼。

**你是藏書館的主人？** 告訴 Lennox：*「我是藏書館主人。」*

### 新增一本 Book

在 Claude Code 中使用 `/new-prompt-doc` 指令。貼上 prompt 全文，Lennox 會自動推斷欄位資訊，確認後將其歸入正確位置。

每本 Book 遵循標準格式：

- Frontmatter：`name`、`version`、`updated`、`status`、`target_user`、`platform`
- 正文區塊：用途 · 使用方式 · 預期效果 · Prompt 內容 · 版本紀錄

### 目前館藏

- **language-learning/**
  - `Korean/` — korean-beginner-conversation-coach
  - `English/` — english-writing-coach
  - `Japanese/` — japanese-beginner-conversation-coach
