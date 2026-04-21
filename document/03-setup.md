---
title: 一鍵初始化
duration: 10
---

# 3. 自動化初始化

我們將使用 `bwai-workshop-tools` 來自動化處理繁瑣的環境設定，包括 Google Cloud 登入、API 啟用、Gemini CLI 認證以及 Python 虛擬環境的建立。

### 執行一鍵設定 (Setup)
在專案根目錄執行以下指令，這會自動完成所有初始化流程：

```bash
bwai-workshop setup --step environment/bwai_env_config.json
```

執行過程中，請注意以下幾點：
1. **Gemini CLI 認證**: 系統會引導您設定 `GOOGLE_CLOUD_PROJECT` 與區域。
2. **GCP 登入**: 系統會跳出認證視窗，請完成登入並選取您的專案。
3. **API 啟用**: 此步驟會啟用 `Cloud Run`、`Vertex AI` 等必要服務。
4. **Python 環境**: 自動建立 `.venv` 並安裝 `requirements.txt` 中的套件。

### 驗證設定 (Verify)
若要確認所有環境是否已正確完成，可以執行驗證指令：

```bash
bwai-workshop verify --step environment/bwai_env_config.json
```

### 啟動虛擬環境
環境設定完成後，請手動啟動 Python 虛擬環境：

```bash
source .venv/bin/activate
```
