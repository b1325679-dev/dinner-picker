# 學生租屋權益知識庫 - AI 開發指南 (AGENTS.md)

## 1. 專案目的
建立大學生租屋法規知識庫。UI 捨棄傳統與手繪風格，全面採用「Glassmorphism (毛玻璃透視風)」，並導入真實 LLM (Gemini API) 驅動的智能客服，提供最準確的法規諮詢。

## 2. 檔案與目錄結構
- `index.html`: 首頁（內建 Gemini API 呼叫邏輯）
- `style.css`: 全域樣式表
- `pages/`: 存放靜態文章檔案

## 3. 全新網頁風格與 UI 規範 (Glassmorphism)
- **背景**：使用動態感的柔和漸層色 (`linear-gradient`，如紫羅蘭與天空藍融合)，呈現現代科技感。
- **卡片設計**：採用半透明白底 (`rgba(255, 255, 255, 0.6)`)、強烈背景模糊 (`backdrop-filter: blur(16px)`)、細緻的白色內邊框，打造磨砂玻璃的懸浮立體感。完全禁止使用粗邊框或點陣圖。
- **AI 聊天室**：懸浮於右下角，同樣採用毛玻璃材質，聊天氣泡具備現代簡約感。

## 4. AI 智能客服 (API) 整合準則
- **捨棄 if-else**：絕對禁止使用寫死的關鍵字判斷。
- **LLM 串接**：使用 JavaScript `fetch` 原生方法呼叫 `generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent`。
- **Prompt 設計**：呼叫 API 時，必須在 System Prompt 限制其身分為「台灣大學生租屋法律顧問」，並要求用簡短白話文回答。
