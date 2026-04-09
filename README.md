# ⬡ Abacus

**Hypermodern spreadsheet for Linux & Windows.**  
Cells as nodes. Data as flow. Intelligence built in.

```
╔═══════════════════════════════════════════════════════════╗
║  ABACUS  1.0.0  —  Hypermodern Spreadsheet                ║
║  Reactive · Graph-native · AI-assisted · Anglo-futurist   ║
╚═══════════════════════════════════════════════════════════╝
```

---

## Philosophy

Traditional spreadsheets treat cells as isolated values.  
Abacus treats cells as **nodes in a computation network**.

Every formula creates an edge. Every dependency is visible.  
The workbook is a directed acyclic graph — you can see it.

---

## Features

### 🧮 Reactive Data Engine
- Cells update dynamically when dependencies change
- Topological evaluation order (Kahn's algorithm)
- Cycle detection with clear `#CIRCULAR` errors
- 40+ built-in functions: SUM, AVERAGE, IF, ROUND, CAGR, GROWTH, …
- Cross-sheet references: `=Sheet2!B3`
- Range functions: `=SUM(A1:A20)`, `=MAX(B2:F10)`

### ⬡ Computation Graph View
Toggle **Grid ↔ Graph** to see your data flow visualised:
- Force-directed layout (nodes settle into dependency order)
- Directed edges with bezier curves and arrowheads
- Colour-coded: formula cells, value cells, error cells
- Drag nodes to rearrange; scroll to zoom; click to select

### 📊 Chart Panel
- Line, Bar, Scatter, Area, Heatmap
- Auto-extracts numeric series from active sheet
- Chart from selection: select a range → Insert → Chart from Selection
- Real-time updates as data changes

### 🤖 AI Assistant (Claude-powered)
- Ask natural-language questions about your data
- Quick prompts: "Forecast next quarter", "Find anomalies", "Summarise data"
- Formula suggestions applied directly to selected cell
- Full workbook context sent with every query
- Requires Anthropic API access

### 🌐 Multi-Sheet Workbooks
- Unlimited sheets; cross-sheet references propagate reactively
- Demo workbook: Sheet1 (data) → Metrics (KPIs) → Forecast (projections)
- Right-click sheet tabs to rename / delete

### 💾 Persistence
- Save/load as `.abacus` (JSON format)
- Full formula and style preservation

---

## Installation

```bash
# Create environment
python -m venv venv
source venv/bin/activate          # Linux/Mac
venv\Scripts\activate             # Windows

# Install dependencies
pip install -r requirements.txt

# Run
python main.py
```

### Requirements
- Python 3.10+
- PySide6 ≥ 6.5
- matplotlib ≥ 3.7 (optional — for charts)
- numpy ≥ 1.24 (optional — for charts)

---

## Keyboard Shortcuts

| Action              | Shortcut            |
|---------------------|---------------------|
| Navigate            | Arrow keys          |
| Edit cell           | Enter / F2 / type   |
| Confirm edit        | Enter / Tab         |
| Cancel edit         | Escape              |
| Copy / Paste / Cut  | Ctrl+C / V / X      |
| Clear cell(s)       | Delete              |
| Select all          | Ctrl+A              |
| New workbook        | Ctrl+N              |
| Open file           | Ctrl+O              |
| Save                | Ctrl+S              |
| Save As             | Ctrl+Shift+S        |
| Multi-select        | Shift + Arrow       |

---

## Formula Reference

```
Aggregates:   SUM, AVERAGE, AVG, MIN, MAX, COUNT, COUNTA, MEDIAN, STDEV, VAR
Math:         ABS, SQRT, POWER, ROUND, FLOOR, CEIL, MOD, LOG, LN, EXP, PI, E
Logic:        IF, AND, OR, NOT, ISNUMBER, ISBLANK, IFERROR
Text:         LEN, UPPER, LOWER, CONCAT, TEXT, LEFT, RIGHT, MID, TRIM
Finance:      GROWTH(start,end,n), CAGR(start,end,years)
```

**Examples:**
```
=SUM(B2:B9)                     Sum a column
=IF(B2>1000000,"Large","Small") Conditional
=ROUND(D2/B2*100,1)             Percentage margin
=CAGR(B2,B9,7)                  Compound annual growth rate
=Sheet2!B3                       Cross-sheet reference
=SUM(Sheet1!B2:B9)              Cross-sheet range
```

---

## Architecture

```
abacus/
├── main.py                 Entry point
├── config.py               Palette, fonts, constants
├── demo.py                 Seed data for demo workbook
│
├── engine/
│   ├── cells.py            Cell model, address parsing
│   ├── graph.py            Dependency graph (DependencyGraph)
│   ├── evaluator.py        Formula parser & evaluator (recursive descent)
│   └── workbook.py         Workbook: sheets + reactive evaluation
│
├── ui/
│   ├── theme.py            Qt stylesheet (Anglo-futurist dark)
│   ├── grid.py             Virtual spreadsheet grid (custom QAbstractScrollArea)
│   ├── graph_view.py       Force-directed computation graph (QWidget)
│   ├── charts.py           Matplotlib chart panel
│   └── main_window.py      Main window assembly
│
└── ai/
    └── assistant.py        AI panel (Claude API via threading)
```

---

## Demo Workbook

On launch, Abacus loads a 3-sheet financial model:

| Sheet    | Contents                                          |
|----------|---------------------------------------------------|
| Sheet1   | Quarterly revenue (8 quarters, formulas for GP/margin/growth) |
| Metrics  | KPI summary — cross-sheet formulas pulling from Sheet1 |
| Forecast | 2025 projections — dependent on Sheet1 AND Metrics |

This demonstrates **reactive multi-sheet computation**: change a revenue figure in Sheet1 and watch Metrics and Forecast update instantly.

Switch to **Graph View** (⬡ Graph) with the Metrics or Forecast sheet active to see the cross-sheet dependency graph.

---

## Visual Design

Anglo-futurist dark palette:

| Role           | Colour    |
|----------------|-----------|
| Background     | `#0A0C0F` |
| Surface        | `#0F1215` |
| Formula cells  | `#1A3A2A` |
| Accent blue    | `#1A6EFF` |
| Gold           | `#C8A84B` |
| Cyan           | `#29C4D8` |
| Text primary   | `#E8EDF3` |

---

*Built with Python, PySide6, matplotlib & Anthropic Claude.*
