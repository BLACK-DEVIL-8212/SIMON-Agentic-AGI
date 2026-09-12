<div align="center">

# 🧠 EDIATH Autonomous AI System

**Production-ready multi-agent AI with voice interaction, local LLM reasoning, and robust agent orchestration.**

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Production--Ready-00C853?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-8A2BE2?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-36BCF7?style=for-the-badge)](CONTRIBUTING.md)

</div>

---

## 📖 Overview

**EDIATH** is an autonomous, production-grade multi-agent AI system designed to reason, orchestrate tasks, and interact via voice. It runs locally using **GGUF-based LLMs**, ensuring privacy, low latency, and zero reliance on external APIs.

Built for stability, EDIATH features **graceful shutdown**, **loop prevention**, and a **crash-resistant architecture** — making it suitable for always-on deployment.

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| 🎙️ **Voice UI + Backend** | Full-duplex voice interaction with a dedicated backend service. |
| 🧠 **LLM Reasoning (GGUF)** | Runs local quantized models via `llama-cpp` for fast, private inference. |
| 🤖 **Agent Orchestration** | Multi-agent coordination for complex, multi-step task execution. |
| 🛡️ **Graceful Shutdown** | Clean resource release and state saving on exit. |
| 🔁 **No Crashes / Loops** | Defensive architecture prevents infinite loops and unexpected failures. |
| ⚡ **Dual-Mode Launcher** | Run as a full voice UI or a headless backend orchestrator. |

---

## 🚀 Quick Start

### Prerequisites
- Python **3.10+**
- A GGUF-format LLM file (e.g., `llama-3-8b-instruct.Q4_K_M.gguf`)
- A working microphone (for UI mode)

### Installation

```bash
# Clone the repository
git clone https://github.com/BLACK-DEVIL-8212/EDIATH-Agentic-AI.git
cd EDIATH-Agentic-AI

# Install in editable mode
pip install -e .
Run
bash
python launcher.py --mode ui
🎛️ Modes
EDIATH supports two distinct runtime modes:

1. ui (Default)
Launches the full voice UI + backend. This is the recommended mode for interactive use.

bash
python launcher.py --mode ui
2. backend
Runs the headless orchestrator only. Ideal for servers, automation pipelines, or API integration.

bash
python launcher.py --mode backend
🔍 Optional Checks
Verify your environment and code integrity before running:

bash
# Check for missing dependencies
python launcher.py --check-deps

# Run syntax validation across all scripts
python scripts/check_syntax.py
🏗️ Architecture
text
┌─────────────────────────────────────────────────────────┐
│                     EDIATH Launcher                      │
│                  (launcher.py --mode)                    │
└───────────────┬─────────────────────────┬───────────────┘
                │                         │
        ┌───────▼───────┐         ┌───────▼───────┐
        │   Voice UI    │         │   Backend     │
        │  (Frontend)   │◄───────►│ Orchestrator  │
        └───────┬───────┘         └───────┬───────┘
                │                         │
                │                 ┌───────▼───────┐
                │                 │  Agent Pool   │
                │                 │ (Multi-Agent) │
                │                 └───────┬───────┘
                │                         │
                └─────────────┬───────────┘
                              │
                      ┌───────▼───────┐
                      │  GGUF LLM     │
                      │  (Local LLM)  │
                      └───────────────┘
📁 Project Structure
text
EDIATH-Agentic-AI/
├── launcher.py              # Main entry point (UI / backend modes)
├── scripts/
│   └── check_syntax.py      # Syntax validation utility
├── src/
│   ├── agents/              # Multi-agent orchestration logic
│   ├── llm/                 # GGUF LLM wrapper & inference
│   ├── ui/                  # Voice UI components
│   └── backend/             # Headless orchestrator
├── pyproject.toml           # Package configuration
└── README.md
🛠️ Tech Stack
Language: Python 3.10+

LLM Runtime: llama-cpp-python (GGUF)

Voice: Speech-to-Text + Text-to-Speech pipeline

Architecture: Modular, event-driven, multi-agent

🤝 Contributing
Contributions are welcome! Please open an issue first to discuss major changes.

Fork the repo

Create your feature branch (git checkout -b feature/amazing-feature)

Commit your changes (git commit -m 'Add amazing feature')

Push to the branch (git push origin feature/amazing-feature)

Open a Pull Request

📜 License
This project is licensed under the MIT License — see the LICENSE file for details.

<div align="center">
Built with 🧠 by Srijan Singh

Autonomous AI that reasons, orchestrates, and executes.

</div> ```
