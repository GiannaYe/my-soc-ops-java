# 🎲 Soc Ops — Social Bingo

> **Find people. Mark squares. Get BINGO!**  
> A hands-on icebreaker game _and_ a VS Code GitHub Copilot Agent workshop in one.

[![Java 21](https://img.shields.io/badge/Java-21-orange?logo=openjdk)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.4-brightgreen?logo=springboot)](https://spring.io/projects/spring-boot)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-purple?logo=github)](https://copilot-dev-days.github.io/agent-lab-java/)

---

## What is Soc Ops?

**Soc Ops** is a Social Bingo game built for in-person mixers and team events. Each player gets a 5×5 board filled with icebreaker prompts — find real people who match each square, mark it off, and race to get **five in a row**!

```
┌─────────────┬─────────────┬─────────────┬─────────────┬─────────────┐
│  Owns a pet │ Morning     │ Speaks 3+   │ Has been to │ Likes spicy │
│             │ person ☀️   │ languages   │ 5 countries │ food 🌶️    │
├─────────────┼─────────────┼─────────────┼─────────────┼─────────────┤
│ Made their  │ Plays a     │ Remote      │ Reads sci-  │ Runs a side │
│ own coffee  │ musical     │ worker 💻   │ fi 🚀       │ project     │
│ today       │ instrument  │             │             │             │
├─────────────┼─────────────┼─────────────┼─────────────┼─────────────┤
│ Has a       │ Night owl   │   ★ FREE ★  │ Loves       │ Traveled    │
│ standing    │ 🦉          │             │ hiking 🏔️  │ solo        │
│ desk        │             │             │             │             │
├─────────────┼─────────────┼─────────────┼─────────────┼─────────────┤
│ Meditates   │ Foodie 🍜   │ Learns      │ Prefers     │ Has lived   │
│ regularly   │             │ coding for  │ dogs 🐕     │ abroad      │
│             │             │ fun         │             │             │
├─────────────┼─────────────┼─────────────┼─────────────┼─────────────┤
│ Watches     │ Loves       │ Board game  │ Tea over    │ Gym regular │
│ anime       │ karaoke 🎤  │ enthusiast  │ coffee ☕   │ 💪          │
└─────────────┴─────────────┴─────────────┴─────────────┴─────────────┘
```

It's also the **starter project** for a hands-on Copilot Agent Mode workshop — you'll use AI agents to redesign, extend, and test it from scratch.

---

## ✨ Features

- 🎯 **5×5 bingo board** with randomized icebreaker prompts
- 🏆 **Win detection** across rows, columns, and diagonals
- 🔄 **New game** resets and reshuffles the board
- 🎨 **Themeable UI** built with Thymeleaf + utility-first CSS
- ⚡ **REST API** — `GET /api/game` · `POST /api/game/move`
- 🚀 **Auto-deploys** to GitHub Pages on every push to `main`

---

## 🧪 Workshop: GitHub Copilot Agent Lab

This repo doubles as a ~1 hour hands-on lab for learning **VS Code Agent Mode** with GitHub Copilot. You'll use agentic workflows to redesign, extend, and test the app — no manual coding required.

### What You'll Learn

| # | Skill | Description |
|---|-------|-------------|
| 1 | **Context Engineering** | Teach AI about your codebase with workspace instructions |
| 2 | **Agentic Primitives** | Background agents, cloud agents, and custom workflows |
| 3 | **Design-First Development** | Let AI iterate on UI while you guide the vision |
| 4 | **Test-Driven Development** | Use TDD agents (Red → Green → Refactor) for reliable features |

### 📚 Lab Guide

| Part | Title | Time |
|------|-------|------|
| [**00**](workshop/00-overview.md) | Overview & Checklist | — |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering | 15 min |
| [**02**](workshop/02-design.md) | Design-First Frontend | 15 min |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master | 10 min |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development | 20 min |

> 📖 Full guide: **[workshop/GUIDE.md](workshop/GUIDE.md)** · also available on [GitHub Pages](https://copilot-dev-days.github.io/agent-lab-java/)

---

## 🚀 Quick Start

**Prerequisites:** [Java 21 JDK](https://adoptium.net/) · [Apache Maven 3.9+](https://maven.apache.org/) (or use the included wrapper)

> 💡 Use the included [Dev Container](.devcontainer) for a zero-setup environment in VS Code!

```bash
# Clone and run
git clone https://github.com/GiannaYe/my-soc-ops-java
cd my-soc-ops-java/socops
./mvnw spring-boot:run
# → Open http://localhost:8080
```

### Other commands

```bash
# Build
./mvnw clean package

# Run tests
./mvnw test
```

---

## 🤝 Contributing

This project follows the [GitHub Community Code of Conduct](CODE_OF_CONDUCT.md).  
See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines and [SECURITY.md](SECURITY.md) to report vulnerabilities.
