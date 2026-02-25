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
- 💾 **可靠儲存**：MySQL 資料庫確保資料安全可靠

## 技術架構

### 後端技術棧
- **框架**: FastAPI
- **資料庫**: PostgreSQL
- **快取**: Redis
- **LLM 整合**: 
- **認證**: JWT 認證
- **部署**: Docker

### 前端技術棧
- **框架**: Vue 3 + Composition API
- **建構工具**: Vite
- **UI 元件庫**: 待定
- **狀態管理**: Pinia
- **路由**: Vue Router
- **HTTP 客戶端**: Axios

## 快速開始

### 資料庫設置

1. 進入資料庫目錄：
```bash
cd database
```

2. 複製環境變數範本並設定：
```bash
cp .env.example .env
```

3. 編輯 `.env` 檔案，設定所需的環境變數：

   | 變數 | 說明 | 預設值 |
   |---|---|---|
   | `POSTGRES_USER` | PostgreSQL 使用者名稱 | — |
   | `POSTGRES_PASSWORD` | PostgreSQL 密碼 | — |
   | `POSTGRES_DB` | PostgreSQL 資料庫名稱 | — |
   | `POSTGRES_PORT` | PostgreSQL 主機端口 | `5432` |
   | `REDIS_PORT` | Redis 主機端口 | `6379` |
   | `REDIS_PASSWORD` | Redis 密碼 | — |

4. 啟動 PostgreSQL 與 Redis：
```bash
docker compose up -d
```

5. 驗證所有服務運行狀態：
```bash
docker compose ps
```

PostgreSQL 將自動使用 `db/init.sql` 中定義的架構進行初始化。Redis 用於會話與 Token 管理。

### 後端設置

即將推出...

### 前端設置

即將推出...

## 資料庫文檔

[`docs/database`](docs/database) 目錄包含完整的資料庫架構文檔：

- **SQL 文件**：完整的資料庫表結構定義
- **ER 圖**：[📊 查看互動式ER圖](https://dbdiagram.io/e/69859812bd82f5fce2dbbe49/6988ca37bd82f5fce2076214)

![ER圖](docs/database/images/dev_u_finder.png)