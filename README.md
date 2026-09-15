# DROS Doctrinal Copilot

Bilingual Obsidian plugin for doctrinal anchoring, retrieval, and synthesis.

雙語 Obsidian 外掛，用於義理錨定、檢索、綜述與筆記回寫。

---

## English

### What it does

DROS Doctrinal Copilot helps you:
- anchor selected text or notes to a doctrinal context
- query a local DROS backend or direct LLM endpoint
- generate structured doctrinal summaries
- save results back into your vault as pavilion notes
- switch between Chinese and English output modes

### Install

1. Copy this folder into your vault at:
   `YOUR_VAULT/.obsidian/plugins/dros-doctrinal-copilot/`
2. Restart Obsidian.
3. Open Settings -> Community plugins and enable DROS Doctrinal Copilot.
4. Open the plugin settings and configure your backend mode and API keys.

### Start the backend

If you are using the DROS backend mode, start the local injector service first.
For this workspace, that is usually the DROS launcher or injector script used by your setup.

### Usage

- Open the command palette and run DROS Doctrinal Copilot commands.
- Use the chat view to ask doctrinal questions or synthesize a passage.
- Use the save button to store generated content as a pavilion note.
- Use the anchor command to connect a selection to its doctrinal context.

### Settings

Common settings include:
- Language mode: auto / zh / en
- Engine mode: direct / proxy / custom
- Prompt injection: contract, nodes, runtime mode
- Custom prompt path and insertion position
- Model and API fields for direct or custom endpoints

### Compatibility

- Version: 1.0.7
- Minimum Obsidian version: 1.8.7

### Release notes for v1.0.7

- Implemented Canonical Passage Penetration Locator: Automatically extracts exact textual passage spans (span:start-end) and T-Number coordinates from long classics (e.g. T0279) when standalone concept notes are absent.
- Enforced Strict Vajra Non-Degradation: Vajra mode strictly prohibits silent fallback to Bodhisattva mode or unauthorized analogies, guaranteeing zero-hallucination canonical grounding.
- Query candidate expansion: Fully incorporates raw queries into candidate discovery for complete doctrinal coverage.

---

## 繁體中文

### 功能簡介

DROS Doctrinal Copilot 提供以下能力：
- 將選取文字或筆記錨定至法義上下文
- 查詢本機 DROS 後端或直連 LLM 端點
- 產出結構化法義摘要與金剛推演
- 將結果儲存回 Vault 的 user_pavilion 筆記
- 支援中英文輸出雙軌切換

### 安裝方式

1. 將本資料夾複製到您的 Vault：
   `您的VAULT/.obsidian/plugins/dros-doctrinal-copilot/`
2. 重啟 Obsidian。
3. 開啟 設定 -> 社群外掛，啟用 DROS Doctrinal Copilot。
4. 在外掛設定中調整您的後端模式與 API Key。

### 啟動後端

若使用 DROS 後端模式，請先啟動本機注入服務。
在此工作區中，通常是您環境所用的 DROS launcher 或注射器腳本。

### 使用方法

- 開啟命令面板，執行 DROS Doctrinal Copilot 相關命令。
- 使用對話檢視詢問法義問題或綜述經文段落。
- 使用儲存按鈕將產生的內容存為 pavilion 筆記。
- 使用錨定命令將選取範圍連接至其法義上下文。

### 設定項目

常見設定包括：
- 語言模式: auto / zh / en
- 引擎模式: direct / proxy / custom
- Prompt 注入: contract, nodes, runtime mode
- 自訂 prompt 路徑與插入位置
- 模型與 API 欄位: 供 direct 或 custom endpoint 使用

### 相容性

- 版本: 1.0.7
- 最低 Obsidian 版本: 1.8.7

### v1.0.7 更新說明

- **實裝長經典物理段落穿透檢索（Passage Penetration Locator）**：當名相筆記不存在時，自動穿透長經典全文（如 T0279）精確標定原典經文切片與 `span` 物理字元座標。
- **鋼性落實金剛模式不降級（Strict Vajra Non-Degradation）**：徹底封堵「查無獨立筆記即偷降級至菩薩模式」的漏洞，全面阻斷電視遙控器等現代比喻與大模型幻覺。
- **全量擴展候選關鍵詞**：Stage 1 自動納入使用者提問原始全文，確保經文偈頌完整命中。

---

## Development

```bash
npm install
npm run build
```

After building, copy main.js into your vault plugin folder if needed.

## 開發

```bash
npm install
npm run build
```

完成 build 後，如需要請將 main.js 複製到 Vault 的外掛資料夾。