# 📿 DROS Doctrinal Copilot — Obsidian 專屬伴學外掛手冊

> **「中文經典背景檢索，高精學術英文合成輸出。」**  
> **"Chinese Canonical Retrieval, Academic English Synthesis."**

DROS Doctrinal Copilot 是為 DROS (Deterministic Runtime OS) 系統量身打造的 Obsidian 官方整合介面，實現高效且高準確性的經典伴學、義理檢索與筆記同步。

---
## 📥 安裝步驟 | Installation Steps

為了啟用並正常執行 DROS 伴學服務，請務必按照以下三步進行配置：

### 第一步：啟用外掛 (Enable Plugin)
1. 本外掛已預置在 `DROS_GitHub_Release` 專案的 `.obsidian/plugins/dros-doctrinal-copilot` 目錄中。
2. 開啟 Obsidian 軟體，進入 `設定 (Settings)` -> `社群外掛載入 (Community Plugins)`。
3. 在 `已安裝外掛 (Installed Plugins)` 列表中，找到 **DROS Doctrinal Copilot** 並點擊啟用。

### 第二步：啟動本地後端服務 (Start Backend Service)
1. 本外掛之高精度檢索與推理邊界控制功能，需依賴本地 DROS 守護進程。
2. 前往專案根目錄，尋找 `雙擊執行-DROS金剛注射器.bat`（或在終端機中執行對應的啟動腳本）。
3. 雙擊執行該批次檔，啟動本地 API 代理服務與知識守護進程，確保後端順利在 `Port 5000` 運行。

### 第三步：喚醒伴學面板 (Launch Copilot)
1. 在 Obsidian 左側功能列中，點擊 **🪷 輪寶圖標 (Dharma Chakra Icon)**。
2. 系統將在右側邊欄展開 DROS Doctrinal Copilot 伴學面板。
3. 您可以立即在對話框中發送您的第一個法義提問，體驗零幻覺的精準 AI 伴學對話！

---

## 💡 極簡操作 SOP | Quick Start SOP

### 1. 發起精準對話
在側邊欄對話框輸入您想研讀的經文、名相或面臨的哲學問題。系統將會自動檢索，召回相應的原典義理進行解答。

### 2. 切換推理合約
根據需要，可在面板頂部即時切換不同的推理合約模式：
*   **📿 金剛合約 (Strict Mode)**：極致嚴謹，AI 將嚴格限制於確定性的經論原典與核心節點範圍內，防範一切隨機幻覺。
*   **🌊 菩薩合約 (Creative Mode)**：高階義理統攝，釋放 AI 的跨學科關聯與邏輯湧現能力。

### 3. 當前筆記智慧關聯
在撰寫研經筆記時，點擊面板上的 `📎 連結當前編輯筆記`，即可將您當前編輯中的筆記上下文無縫帶入 AI 對話，實現隨身研討。

### 4. 一鍵存檔館藏
當 AI 給出具有高度啟發性的答覆時，點擊回覆下方的 `💾 存入館藏` 按鈕，即可一鍵將精美的結構化對話紀錄自動存檔至您的筆記庫中。

---

## 🚀 核心架構：行動端不對稱熔斷與直連降維技術 (Asymmetric Fallback & Direct Ingestion)

為了克服行動裝置 (iOS/Android) 上的網路限制與硬體瓶頸，DROS Doctrinal Copilot 搭載了專門針對 Mobile 的**智能預處理機制**，無需依賴電腦端的 `127.0.0.1` 代理伺服器即可高效運行：

### 1. 物理安全熔斷與降級 (API Route Refactoring)
* **痛點**：手機端無法連線至電腦本機的 Python 網關。
* **機制**：外掛於啟動時自動偵測 `Platform.isMobile`。一旦確認為行動裝置，系統將啟動**物理熔斷**，強制關閉 Proxy 代理模式，並降級為 **Direct 模式 (直連雲端 Google Gemini API)**，確保隨時隨地皆可對話。

### 2. 階梯式 Token 降維看門狗 (Node Dimension Reduction)
* **痛點**：手機網路頻寬與記憶體有限，載入龐大名相庫易導致卡頓或觸發 Token 上限。
* **機制**：讀取本地知識節點時，動態計算上下文長度：
  * 當上下文累計大於 `8,000` 字元時，非核心節點將被**折疊降維至 150 字以內**（僅保留義理路標）。
  * 當累計大於 `12,000` 字元時，直接捨棄非核心節點，防止撐爆大模型上下文。
  * 單一節點上限強制封頂 `10,000` 字，自動截斷超長文本。

### 3. 雲端向量 RAG 備援 (NotebookLM Fallback)
* **痛點**：手機端可能未同步完整的數 GB 大覺藏檔案庫。
* **機制**：當端側檢索不到有效實心名相時，系統會在背景透過腳本或外掛呼叫 **NotebookLM 雲端向量庫** 進行 fallback 召回，確保在手機上也能獲取高品質的經典證據與脈絡。

---

## ⚖️ 專利保護與開源聲明 | Patent Notice & License

- **Patent Notice**: DROS execution governance and security technology is protected under U.S. Provisional Patent Application (U.S. PPA No. 64/111,973, Patent Pending).
- **專利聲明**： DROS 執行治理與安全技術已申請美國臨時專利保護（U.S. Patent Application No. 64/111,973，Patent Pending）。
- **License**: Released under the MIT License. Copyright (c) Top Celestial Company Ltd.

---
*Dros Doctrinal Copilot — 願以此功德，普及於一切。我等與眾生，皆共成佛道。*
