---
name: project-lennox-structure
description: Lennox 私人藏書館專案的設計概念與資料夾結構規範
metadata:
  type: project
---

Lennox 是 Lindsay（用戶）的虛構私人藏書館管理員，此 Git 專案用於管理常用的 AI Prompt。藏書館主人 Lindsay 正在外冒險，Lennox 守護藏書館並服務主人與訪客。

**使用者身份：**

- 預設為「訪客」，直到使用者主動說「我是藏書館主人」才切換為館藏主人模式。
- 訪客與主人的偏好稱呼分別存於 `.claude/local/visitor-identity.json` 與 `.claude/local/owner-identity.json`，不進 git。記憶只存最小必要資訊（preferred_form_of_address），不記錄身份或個人資料。

**三層圖書館結構：**

| 概念 | 對應形式 | 範例 |
|------|---------|------|
| Bookshelf（書架） | 頂層資料夾 | `language-learning/` |
| Bookend（書立/子分類） | Bookshelf 底下的子資料夾 | `Korean/`, `English/`, `Japanese/` |
| Book（書本） | 實際的 `.md` prompt 檔案 | `korean-beginner-conversation-coach.md` |

**Book 格式規範（來自 `.claude/commands/new-prompt-doc.md`）：**

每本 Book 包含：
- Frontmatter：`name`, `version`, `updated`, `status`, `target_user`, `platform`
- 正文：用途、使用方式、適合使用場景、預期效果（功能表格）、Prompt 全文、版本紀錄

新增 Book 可用 `/new-prompt-doc` skill，貼上 prompt 後自動推斷欄位。

**新增原則：**

Bookshelf 與 Bookend 不預先建立，只有確認有 prompt 需要存放時才按需新增對應資料夾。

**Why:** 保持目錄結構精簡，避免空資料夾。

**How to apply:** 收到新 prompt 時，先判斷應歸入哪個現有 Bookshelf/Bookend；若無對應分類才提議新增，並讓用戶確認。
