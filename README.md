# ⬡ Aardvark

Hypermodern computational workspace for Linux & Windows  
Reactive · Graph-native · AI-assisted · Systems-grade

---

## Overview

Aardvark reimagines spreadsheets as **live computation graphs**.

Instead of isolated cells, every value becomes part of a **reactive dependency network**:

- Cells → nodes  
- Formulas → edges  
- Workbooks → computation graphs  

You don’t edit data.  
You shape systems.

---

## Core Features

### 🧮 Reactive Computation Engine
- Real-time dependency propagation
- Topological evaluation ordering
- Cycle detection with `#CIRCULAR` error states
- 40+ built-in functions:
  SUM, AVERAGE, IF, ROUND, CAGR, GROWTH, FORECAST, STDEV, VAR
- Cross-sheet references: `=Sheet2!B3`
- Range evaluation: `=SUM(A1:A20)`

---

### ⬡ Graph View
Visualise spreadsheet logic as a live system:

- Nodes = cells
- Edges = dependencies
- Directed acyclic graph rendering
- Force-directed layout engine
- Interactive manipulation:
  - drag nodes
  - zoom/pan infinite canvas
  - inspect dependency chains

Toggle:
Grid View ↔ Graph View

---

### 📊 Chart Engine
- Line, Bar, Scatter, Area, Heatmap
- Auto-detection of numeric datasets
- “Chart from selection” workflow
- Live updates on data changes
- Fully reactive binding to spreadsheet engine

---

### 🤖 AI Assistant (Claude-powered)
Natural language interface for your data:

Examples:
- Forecast next quarter revenue
- Detect anomalies in KPI trends
- Summarise performance drift across sheets
- Generate optimisation formulas

Features:
- Full workbook context awareness
- Direct formula injection
- Explanation mode
- Suggestive analytics

Requires Anthropic API key.

---

### 🌐 Multi-Sheet System
- Unlimited sheets
- Cross-sheet reactive propagation
- Layered modelling:

Sheet1 → Raw Data  
Sheet2 → Metrics  
Sheet3 → Forecasting  

---

### 💾 Persistence
- Native `.aardvark` file format (JSON-based graph structure)
- Stores:
  - formulas
  - values
  - styles
  - dependency graph
  - metadata
- Optional snapshot/versioning support

---

## Installation

```bash
git clone https://github.com/your-org/aardvark.git
cd aardvark

python -m venv venv
source venv/bin/activate        # Linux / Mac
venv\Scripts\activate           # Windows

pip install -r requirements.txt
python main.py
