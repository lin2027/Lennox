# New Prompt Doc

為一個 Claude Prompt 建立標準格式的說明文件（`.md`）。

## 使用方式

```
/new-prompt-doc
```

直接執行後，貼上 prompt 內容即可。AI 會從 prompt 本身推斷各欄位資訊，只有無法判斷的部分才會詢問。

---

## 執行步驟

### Step 1：收集資訊

請使用者直接貼上 prompt 全文，然後從內容中自動推斷以下欄位：

- **Prompt 名稱**：從 prompt 的目的或語氣歸納一個簡短名稱
- **目標使用者**：從 prompt 中描述的角色或背景推斷（例如「I'm a native Mandarin speaker」→ 母語為中文的使用者）
- **適用平台**：預設為 `Claude Project Instructions`，若 prompt 風格明顯屬於 System Prompt 或 API 則對應調整
- **用途說明**：從 prompt 的指示內容歸納一到兩句話
- **適合的使用場景**：從 prompt 所描述的互動情境推導
- **預期效果 / 功能**：將 prompt 中每條規則轉換為功能說明（用於填表格）
- **存放位置**：根據 prompt 內容的語言或主題猜測目錄（例如內容涉及 Korean → `language-learning/Korean/`）

推斷完成後，列出所有欄位的預設值，**只針對無法從 prompt 內容本身確認的欄位向使用者提問**。確認後再進行下一步。

### Step 2：產生檔案

根據收集到的資訊，用以下模板在指定位置建立 `.md` 檔案。

檔名規則：將名稱轉成 kebab-case，例如 `Korean Input Practice` → `korean-input-practice.md`。

---

## 文件模板

```markdown
---
name: {Prompt 名稱}
version: 1.0.0
updated: {今天日期，格式 YYYY-MM-DD}
status: active
target_user: {目標使用者}
platform: {適用平台}
---

# {Prompt 名稱}

## 用途

{用途說明（一到兩段）}

## 使用方式

1. {平台相關的操作步驟，依 platform 欄位調整說明}
2. ...

### 適合的使用場景

- {場景 1}
- {場景 2}
- ...

## 預期效果

| 功能 | 說明 |
|------|------|
| {功能 1} | {說明 1} |
| {功能 2} | {說明 2} |
| ... | ... |

## Prompt 內容

\```
{Prompt 全文}
\```

## 版本紀錄

| 版本 | 日期 | 異動說明 |
|------|------|---------|
| 1.0.0 | {今天日期} | 初始版本 |
```

---

### Step 3：確認並完成

建立檔案後，輸出：
- 檔案路徑（可點擊）
- 下一次要更新此 prompt 時，提醒使用者：修改 prompt 內容後，同步更新 frontmatter 的 `version`、`updated`，並在版本紀錄表格新增一行。
