# Industrial Digital Twin Platform

> Real-time industrial asset monitoring, predictive maintenance, and 3D visualization platform for Industry 4.0

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-green)](https://nodejs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)](https://www.typescriptlang.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-blue)](https://www.docker.com)

## 🎯 Overview

Enterprise-grade digital twin platform that creates virtual replicas of physical industrial assets (motors, pumps, CNC machines) with real-time IoT telemetry, 3D visualization, and AI-driven predictive maintenance.

**Solves:** Unplanned downtime costs $50B annually in manufacturing. This platform predicts failures 72 hours in advance.

## 🏗️ Architecture

┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│ IoT Sensors │────▶│ Core Service │────▶│ Twin Viewer │
│ (MQTT/OPC-UA)│     │ (Node.js)    │     │ (Three.js)  │
└─────────────┘     └──────┬───────┘     └─────────────┘
                           │
                    ┌──────▼───────┐
                    │ Auth Service │
                    │ Reporting    │
                    └──────────────┘


**Microservices:**
- `auth-service`: JWT, RBAC, OAuth2.0
- `core-service`: Telemetry ingestion, Digital Twin state management
- `reporting-service`: Predictive analytics, Downtime reports
- `twin-viewer`: React + Three.js 3D visualization

## 🚀 Features

- **Real-time Telemetry**: 1000+ sensors, <100ms latency
- **3D Digital Twin**: Three.js, WebGL, GLTF models
- **Predictive Maintenance**: Anomaly detection, Remaining Useful Life (RUL)
- **Role-Based Access**: Operator, Engineer, Admin
- **Audit Logs**: All asset changes tracked

## 🛠️ Tech Stack

**Backend:** Node.js, TypeScript, Express, MQTT, PostgreSQL, Redis, Prisma
**Frontend:** React, TypeScript, Three.js, Zustand, TailwindCSS
**Infra:** Docker, GitHub Actions, OPC-UA

## 📦 Quick Start

```bash
# Clone
git clone https://github.com/Elavarasu_dev/industrial-digital-twin-platform.git
cd industrial-digital-twin-platform

# Setup env
cp .env.example .env

# Docker start (Recommended)
docker-compose up -d

# Or local dev
npm install
npm run dev

Platform: http://localhost:3000
📁 Project Structurejavascriptservices/
  auth-service/       # Authentication & Authorization
  core-service/       # Twin logic & telemetry
  reporting-service/  # Analytics & reports
web/
  twin-viewer/        # 3D Frontend
infrastructure/
  docker/             # Docker configs
docs/                 # Architecture docs🔐 Security
Branch protection on main - No direct pushSecrets in .env - Never committedJWT + RBAC📄 License
MIT © 2026
👤 Author
Built for Industry 4.0 portfolio - [Elavarasu-dev]

