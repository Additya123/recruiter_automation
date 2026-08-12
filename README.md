# Recruiter Automation — AI-Powered Recruitment Workflow Platform

An intelligent automation platform designed to streamline recruitment workflows using AI agents, browser automation, and cloud infrastructure. Orchestrates job scraping, candidate matching, and outreach across multiple job boards.

## Features

✅ **Multi-Agent System**
- Specialized agents for different recruitment tasks
- Job posting analysis with LLM integration
- Hiring plan generation and strategy

✅ **Browser Automation**
- Headless Chrome with BrowserUse framework
- Automated application submissions
- Session management and state persistence

✅ **Indeed & LinkedIn Integration**
- Deterministic and AI-powered scraping agents
- Step-by-step application workflows
- Resume parsing and job matching

✅ **AWS Cloud Deployment**
- CDK infrastructure-as-code setup
- Docker containerization
- CI/CD pipeline ready

✅ **REST API + MCP Server**
- FastAPI backend for agent coordination
- Model Context Protocol (MCP) integration
- GitHub repository automation

## Tech Stack

**Core Technologies**
- Python 3.9+ with FastAPI
- Puppeteer/BrowserUse for browser automation
- LLM agents (OpenAI/Claude integration)
- AWS CDK for infrastructure

**Automation**
- Multiple scraping strategies (deterministic + AI)
- Session management with profile rotation
- Chrome headless browser orchestration

**Cloud & DevOps**
- AWS (EC2, Lambda, CodePipeline)
- Docker for containerization
- GitHub CLI for repo automation
- MCP server for AI agent control

## Project Structure

```
recruiter_automation/
├── agents/                    # Specialized agents
│   ├── indeed_agent.py
│   ├── linkedin_agent.py
│   ├── job_posting_agent.py
│   └── hiring_plan_agent.py
├── browser_sessions/          # Session management
│   ├── runtime/
│   └── scripts/
├── cdk/                       # AWS infrastructure
│   ├── bin/app.ts
│   └── lib/
├── frontend/                  # React UI (Vite)
│   └── src/
├── mcp_server/               # MCP integration
│   └── app.py
├── scripts/                   # Utilities
│   ├── publish_with_gh.py
│   └── prepublish_check.py
├── app.py                    # FastAPI main
├── db.py                     # Database layer
└── requirements.txt
```

## Installation

```bash
# Clone repo
git clone https://github.com/Additya123/recruiter_automation.git
cd recruiter_automation

# Setup Python environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Setup environment variables
cp .env.example .env
# Add your API keys and credentials
```

## Running the Application

### FastAPI Backend

```bash
python app.py
# API runs on http://localhost:8000
```

### Browser Automation

```bash
# Run Indeed agent
python agents/indeed_agent.py

# Run LinkedIn agent
python agents/linkedin_agent.py

# Run hiring plan generator
python agents/hiring_plan_agent.py
```

### MCP Server

```bash
cd mcp_server
python app.py
# Server runs on http://localhost:8001
```

### Frontend

```bash
cd frontend
npm install
npm run dev
# UI runs on http://localhost:5173
```

## Key Agents

| Agent | Purpose |
|-------|---------|
| `indeed_agent.py` | Scrapes and applies to Indeed jobs |
| `linkedin_agent.py` | LinkedIn profile automation |
| `job_posting_agent.py` | Analyzes job descriptions with LLM |
| `hiring_plan_agent.py` | Generates recruitment strategies |

## AWS Deployment

```bash
# From cdk/ directory
npm install
cdk bootstrap
cdk deploy
```

## For Hiring Managers & Recruiters

This project demonstrates:
- **Multi-agent AI systems** — Specialized agents for complex workflows
- **Browser automation** — Puppeteer/BrowserUse at scale
- **Infrastructure automation** — AWS CDK for reproducible deployments
- **Full-stack development** — Python backend + React frontend
- **LLM integration** — Intelligent candidate/job matching
- **DevOps practices** — Docker, CI/CD, infrastructure-as-code

## Challenges Solved

- ✅ Automated job application workflows
- ✅ Resume-to-job matching with AI
- ✅ Multi-platform integration (Indeed, LinkedIn)
- ✅ Scalable cloud infrastructure
- ✅ Session persistence across browser instances

## License

MIT

---

**Documentation:** See [docs/](docs/) for architecture diagrams and detailed guides.
