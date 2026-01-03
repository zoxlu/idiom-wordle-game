# Idiom Wordle Game（四字成語 Wordle）

> **Creative Technologist Portfolio Project**
> An experimental, AI-augmented word game exploring data-driven design, rapid iteration, and human–AI collaboration.

---

## 🎮 Project Overview

**Idiom Wordle Game** is a Wordle-inspired browser game built around **Chinese four-character idioms**.
The project focuses not only on gameplay, but on **system design that supports continuous evolution with AI tools (MCP)**.

This project is designed as a **portfolio piece** demonstrating:

* Front-end system design
* Data-driven content pipelines
* AI-assisted iteration workflows
* Clear separation between content, logic, and presentation

---

## 🧩 Key Features

* Wordle-style guessing mechanics using four-character idioms
* Multiple difficulty tiers reflecting linguistic complexity
* JSON-driven content system (hot-swappable data source)
* Deterministic and non-deterministic game modes (extensible)
* Responsive layout for desktop and mobile
* Designed for AI-in-the-loop iteration (MCP-friendly)

---

## 🧠 Design Philosophy

### 1. Data First

All game content lives outside the codebase in structured JSON.
This allows:

* Rapid content changes without touching logic
* AI-driven regeneration or refinement of datasets
* Versioned evolution of gameplay rules

### 2. Human-in-the-Loop AI

Rather than letting AI regenerate entire systems, this project adopts a **controlled evolution model**:

> *Summarise → Human approval → Targeted modification → New version*

This mirrors real-world AI-assisted creative tooling.

### 3. Progressive Complexity

The project intentionally starts with a **minimal data schema** (string-based idioms) and is designed to scale into richer semantic models without refactoring the game engine.

---

## 📁 Project Structure

```
html-wordle-game/
├─ index.html        # Game UI
├─ style.css         # Styling + RWD
├─ game.js           # Core game logic
├─ data/
│  └─ wordle_game_data.json
├─ README.md
└─ CHANGELOG.md      # Iteration history (AI-assisted)
```

---

## ▶️ Running Locally

Due to browser security restrictions, JSON loading requires a local HTTP server.

```bash
cd idiom-wordle-game
python -m http.server 8000
```

Then open:

```
http://localhost:8000
```

---

## 🌐 Deployment (GitHub Pages)

This project is fully compatible with **GitHub Pages** for zero-backend deployment.

---

## 🚀 Future Directions

* Weighted difficulty selection
* Daily challenge mode (shared seed)
* Idiom explanations & usage examples
* Player statistics stored locally
* Rich semantic dataset upgrade

---

## 🤖 Why MCP (Model Context Protocol) Instead of Prompt-Only AI

This project deliberately adopts **MCP-style, context-aware AI workflows** rather than one-off prompt generation.

### Prompt-Only AI (What This Project Avoids)

* Regenerates entire files
* Loses historical intent
* Breaks working systems
* Difficult to audit or iterate

### MCP-Driven AI (What This Project Demonstrates)

* AI operates on **existing artifacts** (HTML, JSON, specs)
* Changes are scoped, reviewable, and intentional
* Human approval is part of the loop
* Version history remains meaningful

This mirrors how AI tools must behave in **real production environments**, not demos.

---

## 🧪 AI-Driven Feature Exploration (Next Steps)

The following features are intentionally designed to be **simple in implementation but rich in signal** for evaluators:

### 1. Daily Idiom Mode (Deterministic Seed)

* Same idiom for all players per day
* No backend required
* Demonstrates deterministic systems design

### 2. Difficulty-Weighted Sampling

* Idioms selected based on tier and frequency
* Shows data-driven gameplay tuning

### 3. Progressive Disclosure of Meaning

* Explanation revealed only after success
* Reinforces learning-through-play

These features are chosen not for scale, but for **clarity of design thinking**.

---

## 📝 CHANGELOG (AI Iteration Record)

> **Note:** This project maintains a human-readable changelog to document AI-assisted evolution.

Example entry structure:

```md
## v0.3.0 – AI-Assisted Gameplay Refinement
- Introduced MCP-style iteration workflow
- Refactored JSON schema for extensibility
- Improved mobile layout and input handling
- Changes reviewed and approved by human
```

Maintaining this log demonstrates responsible and traceable AI usage.

---

## 👤 Author

This project is part of a **Creative Technologist exploration** into AI-assisted interactive systems.

---

If you are interested in the design approach or iteration workflow, feel free to explore the commit history or reach out for discussion.
