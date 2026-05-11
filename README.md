# CORTEX-OS

## 🎯 Overview
**CORTEX-OS** - Sistema Operacional Linux com IA Auto-Escalável

An innovative Linux-based operating system powered by artificial intelligence, featuring auto-scaling capabilities and intelligent system management.

---

## ✨ Key Features

### 🖥 Graphical Interface
- **KDE Plasma Desktop** (complete environment)
- **SDDM** (modern login screen)
- **Dolphin** (file manager)
- **Konsole** (graphical terminal)

### 🤖 AI & Ollama Integration
- **Ollama** LLM runtime for running AI models locally
- Supports: Mistral, Neural Chat, LLaMA, and more
- Auto-starts on boot
- Models stored in `/opt/cortex-os/models`

### 🧠 Web Control Dashboard
- Access at `http://localhost:5000`
- AI can self-manage through the dashboard
- Download/activate new LLM models
- Install tools (pacman, pip, npm)
- View system logs
- Manage plugins

### 🌐 Integrated Browser
- **Firefox** + **Chromium** pre-installed
- AI can access the internet via browser
- Continuous knowledge updates

### 🔧 Auto-Improvement System
- Python API (`cortex_ai_api.py`)
- AI can install packages automatically
- Create/execute plugins in `/var/lib/cortex-ai/plugins/`
- Complete logging system
- Health check monitoring (Ollama, internet, disk, memory)

### 👤 Security
- No default users (removed)
- Root account locked
- Interactive setup on first boot
- Auto sudo for created user

### 📦 Pre-Installed Tools
- **Development**: Python 3 + pip + virtualenv, Git, GCC, LLVM, CMake, Make
- **Editors**: Vim, Nano
- **Databases**: Redis, SQLite, PostgreSQL
- **Runtime**: Node.js + npm
- **Monitoring**: Prometheus, Grafana
- **Media**: FFmpeg, ImageMagick, SoX
- **Utilities**: Tmux, and more

---

## 🚀 Getting Started

### 1️⃣ Boot the ISO
1. Create VM/USB with the ISO
2. Boot (wait ~30 seconds)
3. SDDM graphical login screen appears

### 2️⃣ Initial Setup
- Create user (e.g., "cortex")
- Set password
- System ready to go

### 3️⃣ Access AI Dashboard
1. Open Firefox or Chromium
2. Navigate to: `http://localhost:5000`

### 4️⃣ What the AI Can Do

**Pull a new LLM model:**
```bash
PUT /api/pull-model {"model": "llama2"}
```

**Install tools:**
```bash
POST /api/install-tool {"tool": "some-package", "type": "pacman"}
```

**Check system health:**
```bash
GET /api/health
```

**Access the internet:**
```bash
firefox &  # AI navigates the web
```

---

## 📊 System Architecture

```
┌─────────────────────────────────┐
│   CortexOS - AI Operating System │
├─────────────────────────────────┤
│  KDE Plasma (GUI)               │
│  Ollama (LLM Runtime)           │
│  Web Dashboard (Control)        │
│  Python API (Auto-Improvement)  │
│  Plugin System                  │
├─────────────────────────────────┤
│  Linux Kernel + Tools           │
└─────────────────────────────────┘
```

---

## 📋 System Requirements

- **Minimum RAM**: 8GB
- **Disk Space**: 3GB (ISO size: 2.95 GB)
- **Virtualization**: VirtualBox, QEMU, or physical machine
- **CPU**: Multi-core recommended

---

## 📚 Next Steps & Suggestions

- [ ] Test in VirtualBox/QEMU with 8GB RAM minimum
- [ ] Create custom AI plugins in `/var/lib/cortex-os/plugins/`
- [ ] Integrate with external APIs (OpenAI, Hugging Face, etc.)
- [ ] Configure CI/CD for automatic OS updates
- [ ] Document your AI use cases

---

## 🎁 Current Status

✅ **BUILD COMPLETE AND SUCCESSFUL!**

- **File**: `cortex-iso-output/cortex-os.iso`
- **Size**: 2.95 GB
- **Status**: 100% ready for deployment

The ISO is fully ready for a self-scaling AI operating system where artificial intelligence can evolve autonomously! 🚀⚡️

---

## 📄 License

*License information coming soon*

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

**Last Updated**: 2026-05-11  

DOWNLOAD E LEITURA - https://drive.google.com/drive/folders/1yKv-SztMmKj9b5HBSfCE1lar5vCj_GjV?usp=sharing
