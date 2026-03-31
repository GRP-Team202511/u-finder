# U Finder
🌍 [English](README.md) | [简体中文](README_zh_cn.md) | **繁體中文**

## 專案簡介

U Finder 是一款基於大語言模型（LLM）的智慧型大學推薦系統。本系統透過分析用戶的學術背景、興趣愛好、職涯規劃等多維度資訊，運用先進的 LLM 技術，為用戶提供個人化的大學推薦服務。

## 主要特色

- 🤖 **智慧推薦**：基于 LLM 的智能分析，提供精準的大學匹配建議
- 💬 **簡單直觀**：可用自然語言直接向 AI 提問，無需進行複雜篩選
- 📊 **資料視覺化**：直觀展示大學資訊與對比分析
- ⚡ **高效能**：基於 FastAPI 的高效能後端 API
- 🎨 **現代化介面**：採用 Vue 3 建構的響應式前端界面
- � **安全保障**：雙因素認證 (2FA)、Passkey/WebAuthn、Cloudflare Turnstile
- 🛡️ **管理員儀表板**：使用者管理、LLM 成本監控、系統日誌
- 💾 **可靠儲存**：PostgreSQL + Redis 確保資料安全與高效能

## 技術架構

### 後端技術棧
- **框架**: FastAPI
- **資料庫**: PostgreSQL
- **快取**: Redis
- **LLM 整合**: Dify
- **認證**: JWT + TOTP 2FA + Passkey/WebAuthn
- **反機器人**: Cloudflare Turnstile
- **部署**: Docker + GitHub Actions CI/CD

### 前端技術棧
- **框架**: Vue 3 + Composition API
- **建構工具**: Vite
- **UI 元件庫**: shadcn-vue
- **狀態管理**: Pinia
- **路由**: Vue Router
- **HTTP 客戶端**: Axios

## 快速開始

### 後端設置

1. 複製儲存庫（含子模組）：

```bash
git clone --recursive https://github.com/GRP-Team202511/u-finder
cd u-finder/backend
```

2. 建立並啟用虛擬環境：

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

3. 安裝相依套件：

```bash
pip install -r requirements.txt
```

4. 配置環境變數：

```bash
cp .env.example .env
# 編輯 .env，填入資料庫、Redis、Dify 和 SMTP 憑證
```

5. 透過 Docker Compose 啟動 PostgreSQL 與 Redis：

```bash
docker compose up -d
```

6. 啟動開發伺服器：

```bash
python run.py
```

API 將在 `http://localhost:8000` 上可用。

更多詳情請參閱[後端 README](backend/README.md)。

### 前端設置

1. 確保已安裝 **Node.js**（v18+）和 **pnpm**（v8+）：

```bash
npm install -g pnpm
```

2. 進入前端使用者應用目錄並安裝相依套件：

```bash
cd frontend/u-finder
pnpm install
```

3. 啟动開發伺服器：

```bash
pnpm dev
```

應用程式將在 `http://localhost:5173` 上可用。

管理員面板請參閱 `frontend/u-finder-admin/`。

更多詳情請參閱[前端 README](frontend/README.md)。

## 資料庫文檔

[`docs/database`](docs/database) 目錄包含完整的資料庫架構文檔：

- **SQL 文件**：完整的資料庫表結構定義
- **ER 圖**：[📊 查看互動式ER圖](https://dbdiagram.io/e/69ae7a43cf54053b6f39329c/69afe47277d079431b482ce0)

![ER圖](docs/database/images/dev_u_finder.png)

## 授權條款

本專案基於 [Apache License 2.0](LICENSE) 授權條款開源。