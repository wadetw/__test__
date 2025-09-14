# Gemini CLI 啟動說明

本文件旨在說明 Gemini CLI (指令列工具) 的啟動與基本使用方式。

---

## 基本啟動

在安裝完成後，您可以直接在終端機 (Terminal) 中輸入以下指令來啟動 Gemini CLI 的互動模式：

```bash
gemini
```

啟動後，您就可以開始與 Gemini 進行對話或下達指令。

## 執行特定指令

除了互動模式，您也可以在啟動時直接帶上指令或參數，讓 Gemini CLI 執行單次任務。

### 顯示幫助訊息

如果您不確定有哪些指令可用，可以隨時查看幫助訊息：

```bash
gemini --help
```

### 執行程式碼或專案相關任務

您可以直接將您的需求以自然語言的方式傳遞給 Gemini CLI。

**範例：**

```bash
# 請求 Gemini 協助修復程式碼中的問題
gemini fix "在 main.py 中加入一個 hello world 函式"

# 請求 Gemini 撰寫一段新的程式碼
gemini write "建立一個 Python 函式來計算費波那契數列"

# 請求 Gemini 解釋一段程式碼
gemini explain "解釋一下這段 React 程式碼的作用"
```

---

**提示：** 具體的指令和功能可能會隨著 Gemini CLI 的版本更新而有所不同。建議隨時使用 `gemini --help` 來獲取最新且最準確的指令列表。