<div align="center">

# 🚀 TablePID

### Modern database client built for developers who move fast

[![License](https://img.shields.io/badge/license-Free_to_use-green)](LICENSE.md)
[![Platform](https://img.shields.io/badge/platform-Windows-blue)]()
[![Version](https://img.shields.io/badge/version-0.1.0-purple)]()

**Stop fighting your database. Start building faster.**

[Download](#download) • [Features](#features) • [Screenshots](#screenshots) • [FAQ](#faq)

---

</div>

## What is TablePID?

TablePID is a modern database client designed for developers, DBAs, and builders who want a fast, beautiful, and AI-powered tool to work with their databases.

**100% Free to Use. No strings attached.**

## Supports

| Database | Status |
|----------|--------|
| PostgreSQL | ✅ Full support |
| MySQL | ✅ Full support |
| MariaDB | ✅ Full support |
| SQLite | ✅ Full support |

---

## Features

### ⚡ AI SQL Assistant

Generate, explain, and optimize SQL with context-aware AI.

```
You: "Ambil 10 user dengan order terbanyak"

AI: SELECT u.id, u.name, COUNT(o.id) as order_count
    FROM users u
    LEFT JOIN orders o ON o.user_id = u.id
    GROUP BY u.id, u.name
    ORDER BY order_count DESC
    LIMIT 10;
```

**AI Providers:**
- Ollama (local, private)
- OpenAI
- Anthropic
- Google Gemini

### 🔒 SSH Tunnel

Connect to remote databases securely with built-in SSH tunneling.

### 📊 ERD Generator

Visualize your database schema with interactive diagrams. Export to PNG.

### 🧠 Context-Aware AI

The AI understands your:
- Database type (PostgreSQL, MySQL, etc.)
- Database version
- Schema and tables
- Foreign keys

So it generates the **correct SQL** for your database.

### 🚀 Query Editor

Monaco-powered editor with:
- Syntax highlighting
- Autocomplete
- Parameterized queries
- Query history

### 🔍 Schema Compare

Compare databases side by side and spot differences instantly.

### 🎨 10 Themes

Dark, Light, Ocean, Forest, Sunset, Purple, Sakura, Candy, Unicorn, Lavender.

---

## Screenshots

> Add screenshots to `release/screenshots/` folder

| Main Interface | ERD Diagram | AI Assistant |
|----------------|-------------|--------------|
| ![Main](screenshots/main.png) | ![ERD](screenshots/erd.png) | ![AI](screenshots/ai.png) |

---

## Keyboard Shortcuts

20+ shortcuts for power users.

| Shortcut | Action |
|----------|--------|
| `Ctrl + Enter` | Run query |
| `Ctrl + Shift + F` | Format SQL |
| `Ctrl + E` | Toggle query editor |
| `Ctrl + Shift + A` | Toggle AI assistant |
| `Ctrl + T` | New tab |
| `Ctrl + W` | Close tab |
| `F1` | Show all shortcuts |

---

## Download

### Windows

**Latest Release: v0.1.0**

[⬇️ Download TablePID v0.1.0](https://github.com/tablepid/tablepid/releases/latest)

- Windows 10/11 (64-bit)
- ~15 MB installer
- No dependencies required

### Installation

1. Download the installer
2. Run the `.msi` file
3. Follow the setup wizard
4. Launch TablePID

---

## Why TablePID?

| Traditional Tools | TablePID |
|-------------------|----------|
| ❌ Outdated UI | ✅ Modern, beautiful |
| ❌ No AI | ✅ AI-powered SQL |
| ❌ Slow & heavy | ✅ Fast & lightweight |
| ❌ Expensive | ✅ 100% Free |
| ❌ Limited themes | ✅ 10 themes |

---

## FAQ

### Is TablePID really free?

Yes! 100% free to use. No premium tiers, no hidden fees.

### Is my data safe?

Your credentials are encrypted in your OS keychain. AI providers only receive your prompts, never your credentials or database data.

### Can I use it offline?

Yes! All features work offline except AI. For AI, use local Ollama for full offline support.

### Is the source code open?

The source code is proprietary, but the app is free to use and distribute.

### How do I report bugs?

Open an issue on GitHub or contact us directly.

---

## Roadmap

- [x] v0.1.0 - Initial release with core features
- [ ] v0.2.0 - Enhanced AI, more providers
- [ ] v0.3.0 - Team features, shared queries
- [ ] v1.0.0 - Stable release, plugins

---

## Made with ❤️

Built for developers who ship fast.

**TablePID** - Modern database client for developers, DBAs and builders.
