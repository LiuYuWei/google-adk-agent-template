---
title: 環境準備
duration: 10
---

# 2. 環境準備

本工作坊強烈建議使用 **Google Cloud Console (Cloud Shell)** 進行。Cloud Shell 是一個預裝了所有必要工具（包括 `gcloud`、`python`、`pip`、`git`）的雲端開發環境，且完全免費。

### 必備條件
1.  **Google Cloud 帳號**: 您需要一個具備帳單帳戶的 GCP 專案。
2.  **啟用 Cloud Shell**: 登入 [Google Cloud Console](https://console.cloud.google.com/) 並點擊右上角的「啟用 Cloud Shell」按鈕。

### 複製專案
在 Cloud Shell 終端機中，執行以下指令：

```bash
git clone https://github.com/LiuYuWei/google-adk-agent-template.git
cd google-adk-agent-template
```

### 安裝自動化工具
為了簡化環境設定流程，我們將使用 `bwai-workshop-tools` 自動化工具：

```bash
pip install bwai-workshop-tools
```

---

### 使用 Gemini CLI 進行工作坊

**Gemini CLI** 是一個強大的終端機 AI 助手，可以協助您理解程式碼、生成測試、甚至自動化執行工作坊步驟。在 Cloud Shell 中已經預裝此工具。

#### 啟動 Gemini CLI
在終端機輸入以下指令啟動：
```bash
gemini
```

#### 實戰用法：自動化協助
您可以要求 Gemini CLI 協助您完成後續步驟：

**範例指令：**
```bash
# 讓 Gemini 幫您解釋專案結構
gemini "請閱讀專案中的關鍵檔案，並向我解釋這個 ADK 專案是如何運作的"

# 讓 Gemini 協助執行後續的 setup 指令
gemini "幫我執行 bwai-workshop setup 並使用 environment/bwai_env_config.json 設定檔"
```

> [!TIP]
> 配合 `bwai-workshop-tools` 與 `Gemini CLI` 使用，可以極大地提升您的開發效率並減少出錯機會！
