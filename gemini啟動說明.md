# Gemini 啟動說明

本文件旨在說明 Gemini 的幾種常見啟動方式。請根據您的具體情況，選擇對應的操作。

---

## 情況一：啟動 Gemini CLI (本工具)

如果您指的是目前正在使用的這個 Gemini 指令列工具，通常在安裝完成後，您可以直接在終端機中啟動。

**基本啟動：**

```bash
gemini
```

**執行特定指令：**

您也可以在啟動時帶上特定的指令或參數，例如：

```bash
# 範例：顯示幫助訊息
gemini --help

# 範例：執行一個特定的修復任務
gemini fix "在 main.py 中加入一個 hello world 函式"
```

---

## 情況二：透過 API 使用 Google Gemini 模型

如果您是開發者，想要在您的應用程式中使用 Google 的 Gemini AI 模型，您需要透過 API 來進行。

### 1. 取得 API 金鑰

首先，您需要前往 [Google AI Studio](https://aistudio.google.com/app/apikey) 取得您的 API 金鑰。

### 2. 在您的專案中啟動

以下提供 Python 和 Node.js 的基本範例：

#### Python 範例

**安裝 SDK:**
```bash
pip install google-generativeai
```

**程式碼 (`main.py`):**
```python
import google.generativeai as genai
import os

# 建議將 API 金鑰儲存在環境變數中
# os.environ['GEMINI_API_KEY'] = "您的API金鑰"

genai.configure(api_key=os.environ['GEMINI_API_KEY'])

# 初始化模型
model = genai.GenerativeModel('gemini-pro')

# 產生內容
response = model.generate_content("請寫一首關於宇宙的詩")

print(response.text)
```

**啟動執行：**
```bash
python main.py
```

#### Node.js (JavaScript) 範例

**安裝 SDK:**
```bash
npm install @google/generative-ai
```

**程式碼 (`index.js`):**
```javascript
const { GoogleGenerativeAI } = require("@google/generative-ai");

// 建議將 API 金鑰儲存在環境變數中
const genAI = new GoogleGenerativeAI(process.env.GEMINI_API_KEY);

async function run() {
  // 初始化模型
  const model = genAI.getGenerativeModel({ model: "gemini-pro"});

  const prompt = "請寫一首關於宇宙的詩";

  const result = await model.generateContent(prompt);
  const response = await result.response;
  const text = response.text();
  console.log(text);
}

run();
```

**啟動執行：**
```bash
node index.js
```

---

## 情況三：啟動一個名為 "Gemini" 的本地專案

如果 "Gemini" 是您本地的一個專案名稱，啟動方式將取決於該專案的技術棧。

*   **對於 Node.js 專案:**
    ```bash
    npm start
    # 或者
    node index.js
    ```

*   **對於 Python 專案:**
    ```bash
    python main.py
    ```

*   **如果是一個可執行檔:**
    ```bash
    ./gemini
    ```

請根據您專案的 `README.md` 或相關文件來確定正確的啟動指令。
