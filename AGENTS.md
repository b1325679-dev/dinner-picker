# 學生租屋權益知識庫 - AI 開發指南 (AGENTS.md)

## 1. 專案目的
建立一個提供大學生租屋法規的知識庫。採用現代化卡片式 UI（Card-based UI），確保閱讀體驗舒適、乾淨且專業。

## 2. 檔案與目錄結構
- `index.html`: 網站首頁
- `css/style.css`: 全域樣式表
- `pages/`: 存放所有具體知識文章的 HTML 檔案 (小寫英文，連字號分隔，如 `deposit-rules.html`)

## 3. 網頁風格與 UI 規範 (Card UI)
- **色系**：背景為淺灰底色 `#f4f7f6`，卡片為純白 `#ffffff`，主色調（標題/連結）使用現代藍 `#2563eb`。
- **排版**：採用卡片式設計（帶有 `box-shadow` 與 `border-radius`），最大寬度 `800px`，內容置中。
- **字體**：`'Segoe UI', system-ui, sans-serif`。

## 4. 頁面 HTML 結構要求
1. 外層必須使用 `<div class="container">` 包覆。
2. 內文區塊必須使用 `<div class="card">` 包覆。
3. 列表需使用 `<ul class="article-list">` 以套用專屬的懸浮動態效果。

## 5. AI 開發準則
- **禁止行內樣式**：絕對禁止在 HTML 中使用 `style="..."`。
- **白話文撰寫**：生成的法規必須轉化為大學生能懂的口語，禁止生硬文言文。
