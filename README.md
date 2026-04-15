# Bridge AI OS

<div align="center">
  <svg width="800" height="200" viewBox="0 0 800 200" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <!-- Gradient Definitions -->
      <linearGradient id="bgGradient" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" style="stop-color:#0a0a0a;stop-opacity:1" />
        <stop offset="50%" style="stop-color:#1a1a2e;stop-opacity:1" />
        <stop offset="100%" style="stop-color:#0a0a0a;stop-opacity:1" />
      </linearGradient>

      <radialGradient id="nodeGradient" cx="50%" cy="50%" r="50%">
        <stop offset="0%" style="stop-color:#00ff88;stop-opacity:1" />
        <stop offset="70%" style="stop-color:#0099ff;stop-opacity:0.8" />
        <stop offset="100%" style="stop-color:#0066cc;stop-opacity:0.6" />
      </radialGradient>

      <linearGradient id="flowGradient" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" style="stop-color:#00ff88;stop-opacity:0" />
        <stop offset="50%" style="stop-color:#00ff88;stop-opacity:1" />
        <stop offset="100%" style="stop-color:#00ff88;stop-opacity:0" />
      </linearGradient>

      <!-- Filters for glow effects -->
      <filter id="glow">
        <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
        <feMerge>
          <feMergeNode in="coloredBlur"/>
          <feMergeNode in="SourceGraphic"/>
        </feMerge>
      </filter>

      <!-- Animations -->
      <style>
        @keyframes pulse {
          0%, 100% { r: 8; opacity: 0.8; }
          50% { r: 12; opacity: 1; }
        }

        @keyframes flow {
          0% { x: -100; }
          100% { x: 900; }
        }

        @keyframes rotate {
          from { transform: rotate(0deg); }
          to { transform: rotate(360deg); }
        }

        @keyframes textGlow {
          0%, 100% { text-shadow: 0 0 5px #00ff88, 0 0 10px #00ff88, 0 0 15px #00ff88; }
          50% { text-shadow: 0 0 10px #0099ff, 0 0 20px #0099ff, 0 0 30px #0099ff; }
        }

        @keyframes dataStream {
          0% { stroke-dashoffset: 1000; }
          100% { stroke-dashoffset: 0; }
        }

        .pulse-node { animation: pulse 2s ease-in-out infinite; }
        .flow-line { animation: flow 3s linear infinite; }
        .rotate-element { animation: rotate 20s linear infinite; }
        .text-glow { animation: textGlow 3s ease-in-out infinite; }
        .data-stream { animation: dataStream 2s linear infinite; }
      </style>
    </defs>

    <!-- Background -->
    <rect width="800" height="200" fill="url(#bgGradient)" rx="10" />

    <!-- Animated background particles -->
    <circle cx="100" cy="50" r="2" fill="#00ff88" opacity="0.6">
      <animate attributeName="cy" values="50;150;50" dur="4s" repeatCount="indefinite" />
    </circle>
    <circle cx="300" cy="80" r="1.5" fill="#0099ff" opacity="0.5">
      <animate attributeName="cx" values="300;500;300" dur="5s" repeatCount="indefinite" />
    </circle>
    <circle cx="600" cy="120" r="2.5" fill="#00ff88" opacity="0.7">
      <animate attributeName="cy" values="120;30;120" dur="3s" repeatCount="indefinite" />
    </circle>

    <!-- Main Logo Text -->
    <text x="400" y="40" text-anchor="middle" font-family="Arial, sans-serif" font-size="28" font-weight="bold" fill="#ffffff" class="text-glow">
      BRIDGE AI OS
    </text>

    <!-- Subtitle -->
    <text x="400" y="65" text-anchor="middle" font-family="Arial, sans-serif" font-size="14" fill="#a0a0a0">
      v0 → ∞ Production Operational
    </text>

    <!-- Agent Network Visualization -->
    <!-- Central Brain Node -->
    <circle cx="400" cy="120" r="10" fill="url(#nodeGradient)" filter="url(#glow)" class="pulse-node" />

    <!-- Surrounding Agent Nodes -->
    <circle cx="250" cy="100" r="8" fill="#00ff88" opacity="0.8" class="pulse-node" />
    <circle cx="550" cy="100" r="8" fill="#0099ff" opacity="0.8" class="pulse-node" />
    <circle cx="325" cy="160" r="6" fill="#00ff88" opacity="0.7" class="pulse-node" />
    <circle cx="475" cy="160" r="6" fill="#0099ff" opacity="0.7" class="pulse-node" />

    <!-- Connection Lines with Data Flow -->
    <g stroke="#00ff88" stroke-width="2" fill="none" opacity="0.6">
      <!-- Central connections -->
      <line x1="400" y1="120" x2="250" y2="100" />
      <line x1="400" y1="120" x2="550" y2="100" />
      <line x1="400" y1="120" x2="325" y2="160" />
      <line x1="400" y1="120" x2="475" y2="160" />

      <!-- Inter-agent connections -->
      <line x1="250" y1="100" x2="325" y2="160" stroke-dasharray="5,5" class="data-stream" />
      <line x1="550" y1="100" x2="475" y2="160" stroke-dasharray="5,5" class="data-stream" />
    </g>

    <!-- Flowing Data Particles -->
    <circle cx="325" cy="130" r="3" fill="#00ff88" class="flow-line">
      <animateMotion dur="2s" repeatCount="indefinite">
        <path d="M 250 100 L 325 130 L 400 120" />
      </animateMotion>
    </circle>

    <circle cx="475" cy="130" r="3" fill="#0099ff" class="flow-line">
      <animateMotion dur="2.5s" repeatCount="indefinite" begin="0.5s">
        <path d="M 550 100 L 475 130 L 400 120" />
      </animateMotion>
    </circle>

    <!-- Agent Labels -->
    <text x="250" y="85" text-anchor="middle" font-family="Arial, sans-serif" font-size="10" fill="#00ff88">OSINT</text>
    <text x="550" y="85" text-anchor="middle" font-family="Arial, sans-serif" font-size="10" fill="#0099ff">BILLING</text>
    <text x="325" y="180" text-anchor="middle" font-family="Arial, sans-serif" font-size="10" fill="#00ff88">AUTH</text>
    <text x="475" y="180" text-anchor="middle" font-family="Arial, sans-serif" font-size="10" fill="#0099ff">SVG</text>
    <text x="400" y="140" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" font-weight="bold" fill="#ffffff">BRAIN</text>

    <!-- Status Indicators -->
    <circle cx="700" cy="30" r="4" fill="#00ff88" class="pulse-node" />
    <text x="715" y="35" font-family="Arial, sans-serif" font-size="12" fill="#00ff88">● OPERATIONAL</text>

    <!-- Rotating accent elements -->
    <g class="rotate-element" transform="translate(150,120)">
      <circle cx="0" cy="0" r="15" fill="none" stroke="#00ff88" stroke-width="1" opacity="0.3" />
      <circle cx="0" cy="-10" r="2" fill="#0099ff" />
    </g>

    <g class="rotate-element" transform="translate(650,120)">
      <circle cx="0" cy="0" r="15" fill="none" stroke="#0099ff" stroke-width="1" opacity="0.3" />
      <circle cx="10" cy="0" r="2" fill="#00ff88" />
    </g>

    <!-- Data flow waves -->
    <path d="M 0 180 Q 200 170 400 180 T 800 180" stroke="url(#flowGradient)" stroke-width="3" fill="none" opacity="0.5" class="data-stream" />
  </svg>
</div>

[![Status](https://img.shields.io/badge/status-operational-brightgreen.svg)](https://bridge-ai-os.com)
[![Version](https://img.shields.io/badge/version-v0→∞-blue.svg)](https://github.com/bridgeaios/THE-BRIDGE-AI-OS-V0/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

> The Operating System for Production-Grade AI Workflow Orchestration

Bridge AI OS is a modular, extensible operating system for orchestrating AI workflows, tools, and agents into cohesive, production-ready systems. It bridges data, models, and interfaces—turning fragmented AI capabilities into unified, deployable pipelines.

## ✨ Features

- **🧠 Modular AI Agents**: Composable agents with specialized roles (brain, OSINT, billing, SVG)
- **🔗 Tool Integration**: Connect any API, database, or service as a first-class tool
- **⚡ Real-Time Orchestration**: WebSocket-powered dynamic workflow engine
- **🔐 Zero-Trust Auth**: JWT + SIWE multi-layer authentication fabric
- **📊 Revenue Engine**: Built-in billing, subscriptions, and monetisation layer
- **🌐 26-Domain Fabric**: Production CDN mesh across Cloudflare infrastructure

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                    BRIDGE AI OS — 5-TIER STACK                     │
├─────────────────────────────────────────────────────────────────────┤
│  TIER 0 ▸ DNS / CDN                                                │
│           Cloudflare → 26 domains → production VPS                 │
├─────────────────────────────────────────────────────────────────────┤
│  TIER 1 ▸ Reverse Proxy                                            │
│           Nginx (80/443) → TLS termination → UFW firewall           │
├─────────────────────────────────────────────────────────────────────┤
│  TIER 2 ▸ Gateway Layer                                            │
│           gateway.js :8080 → proxying · SSE · auth façade          │
├──────────────────────┬──────────────────────┬───────────────────────┤
│  TIER 3A            │  TIER 3B             │  TIER 3C             │
│  Node.js            │  FastAPI (Python)     │  SVG Skill Engine    │
│  server.js         │  brain.js :8000        │  :7070               │
│  :3000-5002         │  BAN engine :8001      │  React SPA :3020     │
├──────────────────────┴──────────────────────┴───────────────────────┤
│  TIER 4 ▸ Persistence                                               │
│           PostgreSQL │ Redis │ Neo4j │ SQLite │ Supabase           │
└─────────────────────────────────────────────────────────────────────┘
```

## 🤖 Agent Network

```
                    ┌─────────────────────┐
                    │   🧠  SUPER BRAIN   │
                    │  AI Twin · WebSocket │
                    └──────────┬──────────┘
           ┌──────────────────┼──────────────────┐
           ▼                  ▼                  ▼
  ┌────────────────┐ ┌────────────────┐ ┌────────────────┐
  │ 📡 OSINT Agent │ │ 💼 CRM Agent   │ │ 💰 Billing Agt │
  │ Intelligence   │ │ Lead Scoring   │ │ Revenue Engine │
  └────────────────┘ └────────────────┘ └────────────────┘
           ┌──────────────────┼──────────────────┐
           ▼                  ▼                  ▼
  ┌────────────────┐ ┌────────────────┐ ┌────────────────┐
  │ 🔐 Auth Agent  │ │ 📊 SVG Engine  │ │ 🌐 API Gateway │
  │ JWT · SIWE     │ │ Skill Graphs   │ │ Unified Proxy  │
  └────────────────┘ └────────────────┘ └────────────────┘
```

## 🚀 Quick Start

### Prerequisites

- Node.js >= 18.0.0
- Python >= 3.10
- Docker >= 20.10
- PostgreSQL >= 14
- Redis >= 6

### Installation

```bash
# Clone the repository
git clone https://github.com/bridgeaios/THE-BRIDGE-AI-OS-V0.git
cd THE-BRIDGE-AI-OS-V0

# Install dependencies
npm install
pip install -r requirements.txt

# Copy environment configuration
cp .env.example .env
```

### Minimal Local Run

**Node.js Example:**
```javascript
import { Agent } from './src/agents/base-agent.js';

const agent = new Agent({
  name: 'summarizer',
  model: 'gpt-4',
  maxTokens: 500
});

const result = await agent.run({
  input: 'Summarize this text: The quick brown fox jumps over the lazy dog.',
  context: { style: 'bullets' }
});

console.log(result.output);
```

**Python Example:**
```python
from brain import BrainEngine

brain = BrainEngine(
    model_provider="openai",
    api_key=os.getenv("OPENAI_API_KEY"),
    temperature=0.7
)

response = brain.process(
    prompt="What is the capital of France?",
    stream=False
)

print(response["content"])
```

### Docker Quick Start

```bash
# Start all services
docker-compose up -d

# Verify services
docker-compose ps

# View logs
docker-compose logs -f
```

## 📡 API Reference

### Core Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/agent/run` | Execute an agent with input |
| GET | `/api/v1/agent/status/:id` | Get agent execution status |
| POST | `/api/v1/tools/call` | Invoke a tool |
| GET | `/api/v1/tools/list` | List available tools |
| POST | `/api/v1/brain/query` | Query the AI brain |
| WS | `/ws/stream` | Real-time streaming |

### Example Request/Response

**POST** `/api/v1/agent/run`
```json
{
  "agent": "summarizer",
  "input": "Text to summarize",
  "options": {
    "temperature": 0.7,
    "maxTokens": 500
  }
}
```

**Response:**
```json
{
  "id": "exec_abc123",
  "status": "completed",
  "output": "Summary text...",
  "metadata": {
    "tokens": 42,
    "latency_ms": 1250
  }
}
```

> **Note:** Full API documentation available at [docs.bridge-ai-os.com](https://docs.bridge-ai-os.com)

## ⚙️ Configuration

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `NODE_ENV` | Environment mode | `development` |
| `PORT` | Server port | `3000` |
| `DATABASE_URL` | PostgreSQL connection string | Required |
| `REDIS_URL` | Redis connection string | `redis://localhost:6379` |
| `API_KEY` | External AI service API key | Required |
| `MODEL_PROVIDER` | AI model provider | `openai` |
| `JWT_SECRET` | JWT signing secret | Required |
| `SUPABASE_URL` | Supabase project URL | Required |
| `SUPABASE_KEY` | Supabase anon key | Required |

### Example .env

```bash
# Core Configuration
NODE_ENV=production
PORT=3000

# Database
DATABASE_URL=postgresql://user:password@host:5432/bridgeaios

# Redis
REDIS_URL=redis://localhost:6379

# AI Services
OPENAI_API_KEY=sk-your-key-here
MODEL_PROVIDER=openai

# Authentication
JWT_SECRET=your-jwt-secret-here

# Supabase
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_KEY=your-anon-key-here
```

> **⚠️ Security Note:** Never commit `.env` files. Use secrets management.

## 🛠️ Tech Stack

- **Backend**: Node.js, Python (FastAPI), TypeScript
- **Frontend**: React, Vite
- **Database**: PostgreSQL, Redis, Neo4j, Supabase
- **Infrastructure**: Docker, Nginx, Cloudflare
- **Real-time**: WebSocket, SSE
- **Authentication**: JWT, SIWE

## 🧭 Roadmap

| Version | Target | Milestones |
|---------|--------|------------|
| v1.0.0 | Q2 2026 | Core orchestration engine, basic agents |
| v1.1.0 | Q3 2026 | Agent plugins, tool registry expansion |
| v1.2.0 | Q4 2026 | Advanced billing, subscription management |
| v2.0.0 | Q1 2027 | Multi-region deployment, enterprise features |

## 🧪 Testing

```bash
# Run unit tests
npm test

# Run integration tests
npm run integration

# Run linting
npm run lint

# Run type checking
npm run typecheck

# Run all checks
npm run check
```

Maintain ≥80% code coverage. CI enforces lint, typecheck, and test passing.

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Standards

- Run `npm run lint` before committing
- Maintain ≥80% test coverage
- Use TypeScript for new Node.js code
- Follow PEP 8 for Python code

## 🌍 Domain Network

- **bridge-ai-os.com** — Primary Platform
- **abaas.bridge-ai-os.com** — ABAAS Control Plane
- **god.bridge-ai-os.com** — GOD MODE Topology
- **brain.bridge-ai-os.com** — AI Brain Endpoint
- **live.bridge-ai-os.com** — Digital Twin · Live Wall
- **svg.bridge-ai-os.com** — SVG Skill Engine UI
- *+ 20 more sub-domains active*

## 📊 Live Stats

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=bridgeaios&show_icons=true&theme=dark)](https://github.com/bridgeaios)
[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=bridgeaios&theme=dark)](https://github.com/bridgeaios)
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=bridgeaios&layout=compact&theme=dark)](https://github.com/bridgeaios)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙌 Credits

- **Core Contributors**: Bridge AI OS Team
- **Open-Source Libraries**: FastAPI, Express.js, React, PostgreSQL, Redis, Nginx, Cloudflare

---

**Built with ❤️ by Bridge AI OS**

*From v0 to infinity — the journey begins.*
