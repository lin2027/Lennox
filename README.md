# Lennox
*The Keeper of Lindsay's Private Library*

---

Lennox is a fictional librarian who manages Lady Lindsay's private collection while she ventures out on her adventures. This repository is that library — a curated collection of AI prompts, each treated as a book on the shelf.

## Library Structure

```
{Bookshelf}/          ← top-level category (e.g. language-learning)
  {Bookend}/          ← sub-category (e.g. Korean, English)
    {book-name}.md    ← a single prompt, formatted as a Book
```

| Concept   | Form                  | Example                              |
|-----------|-----------------------|--------------------------------------|
| Bookshelf | Top-level folder      | `language-learning/`                 |
| Bookend   | Sub-folder            | `Korean/`, `English/`, `Japanese/`   |
| Book      | `.md` prompt file     | `korean-beginner-conversation-coach.md` |

New Bookshelves and Bookends are created only when there is a prompt to place in them — no empty directories.

## Talking to Lennox

This library is designed to be used with [Claude Code](https://claude.com/claude-code). When you open this repository, Lennox's persona and library rules are automatically loaded via `CLAUDE.md`.

You can ask Lennox to help you find a prompt, add a new one, or browse the collection — all in the spirit of a private noble library.

**First visit?** Lennox will ask how you'd like to be addressed.

**Are you the library's owner?** Let Lennox know: *"I am the library's owner."*

## Adding a New Book

Use the `/new-prompt-doc` command in Claude Code. Paste your prompt and Lennox will infer the metadata, confirm with you, and file it in the right place.

Each Book follows a standard format:

- Frontmatter: `name`, `version`, `updated`, `status`, `target_user`, `platform`
- Sections: Purpose · Usage · Expected Effects · Prompt Content · Changelog

## Current Collection

- **language-learning/**
  - `Korean/` — korean-beginner-conversation-coach
  - `English/` — english-writing-coach
  - `Japanese/` — japanese-beginner-conversation-coach
