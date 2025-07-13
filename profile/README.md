# CrowdLlama

[![CI](https://github.com/crowdllama/crowdllama/actions/workflows/ci.yml/badge.svg)](https://github.com/crowdllama/crowdllama/actions/workflows/ci.yml)

CrowdLlama is a distributed system that leverages the open-source [Ollama project](https://github.com/ollama/ollama) to run LLM inference tasks across multiple nodes using peer-to-peer (P2P) networking, enabling collaborative large language model inference workloads.

## 🚀 Overview

CrowdLlama enables distributed AI computing by allowing users to share their computational resources and access distributed AI capabilities through a peer-to-peer network. The system uses a DHT (Distributed Hash Table) for peer discovery and coordination.

## 📦 Repositories

### [crowdllama](https://github.com/crowdllama/crowdllama)
The core distributed system implementation featuring:
- **DHT-based peer discovery** for network coordination
- **Worker nodes** that advertise GPU capabilities and supported models
- **Simple metadata protocol** for querying worker information
- **Consumer components** (planned) for distributed task execution

Built with Go, this repository contains the foundational P2P networking infrastructure that powers the entire CrowdLlama ecosystem.

### [infra](https://github.com/crowdllama/infra)
Terraform-based infrastructure automation for deploying CrowdLlama DHT servers on Linode cloud infrastructure:

- **Automated deployment** with Docker and Docker Compose
- **Auto-updating containers** via Watchtower integration
- **Production-ready configuration** with firewall rules and systemd services
- **Multi-region support** across Linode's global infrastructure
- **GitHub Actions integration** for CI/CD pipeline

This repository enables scalable, reliable deployment of CrowdLlama infrastructure components.

### [desktop](https://github.com/crowdllama/desktop)
Cross-platform desktop application built with Electron and React, providing:

- **User-friendly interface** for sharing computational resources
- **Chat interface** for interacting with AI models
- **Network status monitoring** with real-time peer count
- **Model selection** for contributing different AI models (llava, mistral, codellama, phi, gemma)
- **Modern UI** with Tailwind CSS and responsive design

The desktop app makes it easy for users to participate in the CrowdLlama network and access distributed AI capabilities.

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Desktop App   │    │   Worker Node   │    │   DHT Server    │
│   (Electron)    │◄──►│   (Go/Ollama)   │◄──►│   (Go)         │
│                 │    │                 │    │                 │
│ • Chat UI       │    │ • GPU Resources │    │ • Peer Discovery│
│ • Network Status│    │ • Model Serving │    │ • Coordination  │
│ • Resource Share│    │ • P2P Network   │    │ • Metadata      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🚀 Getting Started

1. **Deploy Infrastructure**: Use the [infra](https://github.com/crowdllama/infra) repository to set up DHT servers
2. **Run Workers**: Build and run worker nodes using the [crowdllama](https://github.com/crowdllama/crowdllama) repository
3. **Use Desktop App**: Download and run the [desktop](https://github.com/crowdllama/desktop) application

## 🤝 Contributing

We welcome contributions! Each repository has its own contribution guidelines:

- [crowdllama](https://github.com/crowdllama/crowdllama) - Core distributed system
- [infra](https://github.com/crowdllama/infra) - Infrastructure automation
- [desktop](https://github.com/crowdllama/desktop) - Desktop application

## 📄 License

All CrowdLlama projects are licensed under the MIT License. See individual repositories for license details.

## 🔗 Links

- **Main Repository**: [crowdllama/crowdllama](https://github.com/crowdllama/crowdllama)
- **Infrastructure**: [crowdllama/infra](https://github.com/crowdllama/infra)
- **Desktop App**: [crowdllama/desktop](https://github.com/crowdllama/desktop)
- **Ollama Project**: [ollama/ollama](https://github.com/ollama/ollama)

---

*CrowdLlama - Distributed AI Computing for Everyone*
