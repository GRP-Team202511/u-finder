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
- � **Security**: Two-factor authentication (2FA), Passkey/WebAuthn, Cloudflare Turnstile
- 🛡️ **Admin Dashboard**: User management, LLM cost monitoring, system logs
- 💾 **Reliable Storage**: PostgreSQL + Redis ensures secure and high-performance data management

## Technical Architecture

### Backend Stack
- **Framework**: FastAPI
- **Database**: PostgreSQL
- **Cache**: Redis
- **LLM Integration**: Dify
- **Authentication**: JWT + TOTP 2FA + Passkey/WebAuthn
- **Anti-Bot**: Cloudflare Turnstile
- **Deployment**: Docker + GitHub Actions CI/CD

### Frontend Stack
- **Framework**: Vue 3 + Composition API
- **Build Tool**: Vite
- **UI Component Library**: shadcn-vue
- **State Management**: Pinia
- **Routing**: Vue Router
- **HTTP Client**: Axios

## Quick Start

### Backend Setup

1. Clone the repository with submodules:

```bash
git clone --recursive https://github.com/GRP-Team202511/u-finder
cd u-finder/backend
```

2. Create and activate a virtual environment:

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Set up environment variables:

```bash
cp .env.example .env
# Edit .env with your database, Redis, Dify, and SMTP credentials
```

5. Start PostgreSQL and Redis via Docker Compose:

```bash
docker compose up -d
```

6. Start the development server:

```bash
python run.py
```

The API will be available at `http://localhost:8000`.

For more details, see the [Backend README](backend/README.md).

### Frontend Setup

1. Ensure **Node.js** (v18+) and **pnpm** (v8+) are installed:

```bash
npm install -g pnpm
```

2. Navigate to the frontend user application and install dependencies:

```bash
cd frontend/u-finder
pnpm install
```

3. Start the development server:

```bash
pnpm dev
```

The application will be available at `http://localhost:5173`.

For the admin panel, see `frontend/u-finder-admin/`.

For more details, see the [Frontend README](frontend/README.md).

## Database Documentation

The [`docs/database`](docs/database) directory contains comprehensive database schema documentation:

- **SQL Files**: Complete database table structure definitions
- **ER Diagram**: [📊 View Interactive ER Diagram](https://dbdiagram.io/e/69ae7a43cf54053b6f39329c/69afe47277d079431b482ce0)

![ER Diagram](docs/database/images/dev_u_finder.png)

## License

This project is licensed under the [Apache License 2.0](LICENSE).