# U Finder
🌍 **English** | [简体中文](README_zh_cn.md) | [繁體中文](README_zh_tw.md)

## Project Overview

U Finder is an intelligent university recommendation system powered by large language models (LLMs). By analyzing users' academic backgrounds, personal interests, career plans, and other multidimensional information, the system utilizes advanced LLM technology to provide personalized university recommendation services.

## Key Features

- 🤖 **Smart Recommendations**: LLM-based intelligent analysis delivers accurate university matching suggestions
- 💬 **Simple & Intuitive**: Ask the AI questions directly in natural language—no complex filtering required
- 📊 **Data Visualization**: Intuitive display of university information and comparative analysis
- ⚡ **High Performance**: FastAPI-based high-performance backend API
- 🎨 **Modern UI**: Responsive frontend built with Vue 3
- 💾 **Reliable Storage**: MySQL database ensures secure and reliable data management

## Technical Architecture

### Backend Stack
- **Framework**: FastAPI
- **Database**: PostgreSQL
- **Cache**: Redis
- **LLM Integration**: 
- **Authentication**: JWT Authentication
- **Deployment**: Docker

### Frontend Stack
- **Framework**: Vue 3 + Composition API
- **Build Tool**: Vite
- **UI Component Library**: TBD
- **State Management**: Pinia
- **Routing**: Vue Router
- **HTTP Client**: Axios

## Quick Start

### Database Setup

1. Navigate to the database directory:
```bash
cd database
```

2. Copy the environment template and configure your settings:
```bash
cp .env.example .env
```

3. Edit `.env` file with your preferred credentials. The following variables are required:

   | Variable | Description | Default |
   |---|---|---|
   | `POSTGRES_USER` | PostgreSQL username | — |
   | `POSTGRES_PASSWORD` | PostgreSQL password | — |
   | `POSTGRES_DB` | PostgreSQL database name | — |
   | `POSTGRES_PORT` | PostgreSQL host port | `5432` |
   | `REDIS_PORT` | Redis host port | `6379` |
   | `REDIS_PASSWORD` | Redis password | — |

4. Start PostgreSQL and Redis:
```bash
docker compose up -d
```

5. Verify all services are running:
```bash
docker compose ps
```

PostgreSQL will be initialized automatically with the schema defined in `db/init.sql`. Redis is used for session/token management.

### Backend Setup

Coming soon...

### Frontend Setup

Coming soon...

## Database Documentation

The [`docs/database`](docs/database) directory contains comprehensive database schema documentation:

- **SQL Files**: Complete database table structure definitions
- **ER Diagram**: [📊 View Interactive ER Diagram](https://dbdiagram.io/e/69ae7a43cf54053b6f39329c/69afe47277d079431b482ce0)

![ER Diagram](docs/database/images/dev_u_finder.png)

## License

This project is licensed under the [Apache License 2.0](LICENSE).