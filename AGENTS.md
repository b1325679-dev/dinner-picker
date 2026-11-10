# 學生租屋權益知識庫 - AI 開發指南 (AGENTS.md)

## 1. 專案目的
建立大學生租屋法規知識庫。採用「手帳筆記風（Notebook Style）」，結合點陣背景與標籤卡片，打造友善、無壓力的閱讀體驗，並內建前端 AI 客服。

## 2. 檔案與目錄結構
- `index.html`: 首頁（包含 AI 小助手 UI）
- `style.css`: 全域樣式表
- `pages/deposit-rules.html`: 押金法規頁
- `pages/repair-rules.html`: 修繕法規頁

## 3. 網頁風格與 UI 規範
- **背景**：淺米色底 `#FDFBF7` 搭配灰色點陣圖案（Polka dot grid）。
- **排版 (Grid)**：首頁選單必須使用 CSS Grid (`grid-template-columns`) 並排顯示卡片，減少畫面邊緣留白。
- **卡片設計**：圓角白底，帶有深藍色粗邊框 `#2C3E50` 與稍微偏移的實色陰影（Offset Box-shadow），營造立體貼紙感。卡片上方加入偽元素紙膠帶裝飾。
- **字體**：基礎大小提升至 `18px`，顏色 `#333333`。

## 4. AI 助手開發準則
- **懸浮視窗**：聊天室必須固定於畫面右下角 (`position: fixed; bottom: 20px; right: 20px;`)。
- **對話邏輯**：JavaScript 需攔截使用者的 Enter 鍵，並依據「押金」、「修繕」、「提前解約」等關鍵字給予對應的法規解答。
