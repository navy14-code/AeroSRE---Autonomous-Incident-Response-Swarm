# 🚀 AeroSRE - Autonomous Incident Response Swarm

AeroSRE is an experimental multi-agent AI system designed to automate Site Reliability Engineering (SRE) tasks. It autonomously ingests production logs, identifies root causes, writes patches, and verifies them in a sandboxed environment.

## 🧠 Core Architecture
- **Agent A (Observer):** Hooks into Datadog/Prometheus streams.
- **Agent B (Contextualizer):** RAG-based context retrieval from GitHub repositories.
- **Agent C (Fixer):** Generates and verifies code patches using LLMs.

## ⚙️ Quick Start
\`\`\`bash
pip install -r requirements.txt
cp .env.example .env
# Add your API keys (MiMo, Datadog, GitHub) to .env
python agent_orchestrator.py
\`\`\`

> **Note:** This project heavily relies on large context windows (128k+) for processing massive log files and repository structures.
