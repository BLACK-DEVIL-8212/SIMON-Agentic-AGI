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

**EDIATH** is an autonomous, production-grade multi-agent AI system that reasons, orchestrates tasks, and interacts via voice. It runs locally using **GGUF-based LLMs**, ensuring privacy, low latency, and zero reliance on external APIs.

Built for stability, EDIATH features **graceful shutdown**, **loop prevention**, and a **crash-resistant architecture** — making it suitable for always-on deployment.

---

## ✨ Key Features

- 🎙️ **Voice UI + Backend** — Full-duplex voice interaction with a dedicated backend service
- 🧠 **LLM Reasoning (GGUF)** — Local quantized models via `llama-cpp` for fast, private inference
- 🤖 **Agent Orchestration** — Multi-agent coordination for complex, multi-step tasks
- 🛡️ **Graceful Shutdown** — Clean resource release and state saving on exit
- 🔁 **No Crashes / Loops** — Defensive architecture prevents infinite loops and failures
- ⚡ **Dual-Mode Launcher** — Run as a full voice UI or headless backend orchestrator

---

## 🚀 Quick Start

### Prerequisites
- Python **3.10+**
- A GGUF-format LLM file (e.g., `llama-3-8b-instruct.Q4_K_M.gguf`)
- A working microphone (for UI mode)

### Installation & Run

Run all commands below in a single terminal session:

```bash
# 1. Install the package in editable mode
pip install -e .

# 2. Launch the full voice UI + backend (default mode)
python launcher.py --mode ui

# 3. Optional: Run the headless backend orchestrator only
# python launcher.py --mode backend

# 4. Optional: Check for missing dependencies
# python launcher.py --check-deps

# 5. Optional: Run syntax validation across all scripts
# python scripts/check_syntax.py.
```


### 🎛️ Modes
EDIATH supports two runtime modes:

Mode	Description
ui (default)	Full voice UI + backend — recommended for interactive use
backend	Headless orchestrator — ideal for servers, pipelines, or API integration
To switch modes, simply change the --mode flag:

```bash
python launcher.py --mode ui       # Full voice UI + backend
python launcher.py --mode backend  # Headless orchestrator only
```

### 🏗️ Architecture

```bash
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
```

### 📁 Project Structure
```bash 
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
```

### 🛠️ Tech Stack

- Language: Python 3.10+

- LLM Runtime: llama-cpp-python (GGUF)

- Voice: Speech-to-Text + Text-to-Speech pipeline

- Architecture: Modular, event-driven, multi-agent

### 🤝 Contributing

Contributions are welcome! Please open an issue first to discuss major changes.

- Fork the repo

- Create your feature branch (git checkout -b feature/amazing-feature)

- Commit your changes (git commit -m 'Add amazing feature')

- Push to the branch (git push origin feature/amazing-feature)

- Open a Pull Request

### 📜 License
This project is licensed under the MIT License — see the LICENSE file for details.

---

<div align="center">

  <h3>🧠 Built by <a href="https://github.com/BLACK-DEVIL-8212">Srijan Singh</a></h3>
  
  <p><i>Autonomous AI that reasons, orchestrates, and executes.</i></p>
  
  <br>
  
  <a href="https://github.com/BLACK-DEVIL-8212/EDIATH-Agentic-AI/stargazers">
    <img src="https://img.shields.io/github/stars/BLACK-DEVIL-8212/EDIATH-Agentic-AI?style=for-the-badge&color=36BCF7&labelColor=000000" alt="Stars" />
  </a>
  &nbsp;
  <a href="https://github.com/BLACK-DEVIL-8212/EDIATH-Agentic-AI/network/members">
    <img src="https://img.shields.io/github/forks/BLACK-DEVIL-8212/EDIATH-Agentic-AI?style=for-the-badge&color=8A2BE2&labelColor=000000" alt="Forks" />
  </a>
  &nbsp;
  <a href="https://github.com/BLACK-DEVIL-8212/EDIATH-Agentic-AI/issues">
    <img src="https://img.shields.io/github/issues/BLACK-DEVIL-8212/EDIATH-Agentic-AI?style=for-the-badge&color=00C853&labelColor=000000" alt="Issues" />
  </a>

  <br><br>
  
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:36BCF7,100:8A2BE2&height=120&section=footer&text=Reason.%20Orchestrate.%20Execute.&fontSize=18&fontColor=ffffff&fontAlignY=75&animation=twinkling" width="100%" />

</div>
