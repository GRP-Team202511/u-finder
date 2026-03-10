# U Finder
🌍 [English](README.md) | **简体中文** | [繁體中文](README_zh_tw.md)

## 项目简介

U Finder 是一个基于大语言模型（LLM）的智能大学推荐系统。该系统通过分析用户的学习背景、兴趣爱好、职业规划等多维度信息，利用先进的LLM技术为用户提供个性化的大学推荐服务。

## 主要特性

- 🤖 **智能推荐**: 基于LLM的智能分析，提供精准的大学匹配建议
- 💬 **简单直观**: 可用自然语言直接向AI进行提问，无需进行复杂筛选
- 📊 **数据可视化**: 直观展示大学信息和对比分析
- ⚡ **高性能**: 基于FastAPI的高性能后端API
- 🎨 **现代化UI**: 采用Vue 3构建的响应式前端界面
- 💾 **可靠存储**: MySQL数据库确保数据安全可靠

## 技术架构

### 后端技术栈
- **框架**: FastAPI
- **数据库**: PostgreSQL
- **缓存**: Redis
- **LLM集成**: 
- **认证**: JWT认证
- **部署**: Docker

### 前端技术栈
- **框架**: Vue 3 + Composition API
- **构建工具**: Vite
- **UI组件库**: TBD
- **状态管理**: Pinia
- **路由**: Vue Router
- **HTTP客户端**: Axios

## 快速开始

### 数据库设置

1. 进入数据库目录：
```bash
cd database
```

2. 复制环境变量模板并配置：
```bash
cp .env.example .env
```

3. 编辑 `.env` 文件，配置所需的环境变量：

   | 变量 | 说明 | 默认值 |
   |---|---|---|
   | `POSTGRES_USER` | PostgreSQL 用户名 | — |
   | `POSTGRES_PASSWORD` | PostgreSQL 密码 | — |
   | `POSTGRES_DB` | PostgreSQL 数据库名 | — |
   | `POSTGRES_PORT` | PostgreSQL 宿主机端口 | `5432` |
   | `REDIS_PORT` | Redis 宿主机端口 | `6379` |
   | `REDIS_PASSWORD` | Redis 密码 | — |

4. 启动 PostgreSQL 和 Redis：
```bash
docker compose up -d
```

5. 验证所有服务运行状态：
```bash
docker compose ps
```

PostgreSQL 将自动使用 `db/init.sql` 中定义的架构进行初始化。Redis 用于会话与 Token 管理。

### 后端设置

即将推出...

### 前端设置

即将推出...

## 数据库文档

[`docs/database`](docs/database) 目录包含完整的数据库架构文档：

- **SQL文件**: 完整的数据库表结构定义
- **ER图**: [📊 查看交互式ER图](https://dbdiagram.io/e/69ae7a43cf54053b6f39329c/69afe47277d079431b482ce0)

![ER图](docs/database/images/dev_u_finder.png)

## 许可证

本项目基于 [Apache License 2.0](LICENSE) 许可证开源。