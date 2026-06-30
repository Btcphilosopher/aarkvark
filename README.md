⬡ Aardvark

Hypermodern computational workspace for Linux & Windows.
Cells as intelligence. Data as topology. Spreadsheets reimagined as living systems.

╔═══════════════════════════════════════════════════════════╗
║  AARDVARK  1.0.0  —  Hypermodern Data Engine              ║
║  Reactive · Graph-native · AI-assisted · Systems-grade    ║
╚═══════════════════════════════════════════════════════════╝
Philosophy

Traditional spreadsheets treat data as static grid entries.

Aardvark treats data as a living computation graph.

Every cell is a node.
Every formula is a relationship.
Every workbook is a structured intelligence network.

You don’t “edit cells” — you shape a system of dependencies.

Features
🧮 Reactive Data Engine
Real-time recalculation across dependency graph
Deterministic topological evaluation (Kahn-based ordering)
Cycle detection with explicit #CIRCULAR resolution states
40+ core functions:
SUM, AVERAGE, IF, ROUND, CAGR, GROWTH, FORECAST, VAR, STDEV, …
Cross-sheet references: =Sheet2!B3
Range computation: =SUM(A1:A20), =MAX(B2:F10)
⬡ Computation Graph View

Toggle between Grid ↔ Graph to reveal underlying structure:

Force-directed dependency layout
Directed edges rendered as computational flows
Node types:
value nodes
formula nodes
error nodes
Interactive manipulation:
drag nodes to reshape topology
zoom/pan infinite workspace
click-to-inspect dependency chains
📊 Chart Intelligence Panel
Line / Bar / Scatter / Area / Heatmap visualisations
Auto-detection of numeric series
“Chart from Selection” pipeline
Live re-rendering on data mutation
Reactive binding between chart and cell graph
🤖 AI Computation Assistant (Claude-powered)

Natural-language interface to your dataset:

“Forecast next quarter using exponential smoothing”
“Detect anomalies in revenue stream”
“Summarise KPI drift across sheets”
“Generate optimisation formula for margins”

Capabilities:

Full workbook context injection
Cell-aware reasoning
Direct formula insertion into selected nodes
Explanation mode for computed outputs

Requires Anthropic API access.

🌐 Multi-Sheet Intelligence System
Unlimited interconnected sheets
Cross-sheet dependency propagation
Reference chaining across entire workbook graph

Example pipeline:

Sheet1 → raw data ingestion
Sheet2 → KPI transformation
Sheet3 → predictive modelling layer

Right-click sheet tabs:

rename
duplicate
delete
lock (read-only mode)
💾 Persistence Layer
Native .aardvark format (JSON-based structured graph)
Full preservation:
formulas
styles
dependency graph
metadata annotations
Snapshot versioning support (optional)
Installation
# Create environment
python -m venv venv
source venv/bin/activate        # Linux / Mac
venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt

# Run
python main.py
Requirements
Python 3.10+
PySide6 ≥ 6.5
matplotlib ≥ 3.7 (optional charts engine)
numpy ≥ 1.24 (numerical acceleration layer)
Keyboard System
Action	Shortcut
Navigate	Arrow keys
Edit cell	Enter / F2
Confirm edit	Enter / Tab
Cancel edit	Escape
Copy / Paste / Cut	Ctrl+C / V / X
Clear	Delete
Select all	Ctrl+A
New workbook	Ctrl+N
Open	Ctrl+O
Save	Ctrl+S
Save As	Ctrl+Shift+S
Multi-select	Shift + Arrow
Formula System
Core Functions

SUM, AVERAGE, MIN, MAX, COUNT, MEDIAN, STDEV, VAR, COUNTA

Math Layer

ABS, SQRT, POWER, ROUND, FLOOR, CEIL, MOD, LOG, LN, EXP, PI, E

Logic Layer

IF, AND, OR, NOT, ISNUMBER, ISBLANK, IFERROR

Text Layer

LEN, UPPER, LOWER, CONCAT, TEXT, LEFT, RIGHT, MID, TRIM

Financial Layer

GROWTH(start,end,n), CAGR(start,end,years), FORECAST()

Examples
=SUM(B2:B9)                        Sum column
=IF(B2>1000000,"Large","Small")   Conditional logic
=ROUND(D2/B2*100,1)               Percentage transform
=CAGR(B2,B9,7)                    Growth modelling
=Sheet2!B3                        Cross-sheet reference
=SUM(Sheet1!B2:B9)                Cross-sheet aggregation
Architecture
aardvark/
├── main.py                 Entry point
├── config.py               Theme system + constants
├── demo.py                 Sample workbook generator
│
├── engine/
│   ├── cells.py            Cell model + address parsing
│   ├── graph.py            Dependency graph core
│   ├── evaluator.py        Formula engine (recursive descent parser)
│   └── workbook.py         Multi-sheet reactive system
│
├── ui/
│   ├── theme.py            Anglo-futurist styling system
│   ├── grid.py             Spreadsheet rendering engine
│   ├── graph_view.py       Interactive computation graph
│   ├── charts.py           Visualization layer
│   └── main_window.py      Application shell
│
└── ai/
    └── assistant.py        Claude-powered reasoning layer
Demo Workbook

On launch, Aardvark loads a structured 3-layer system:

Sheet	Role
Sheet1	Raw financial data (8 quarters)
Metrics	KPI transformations + derived indicators
Forecast	Predictive modelling + projections
Behaviour

A change in Sheet1 propagates instantly:

Metrics recalculates KPIs
Forecast updates predictions
Graph view reshapes dependency topology in real time

Switch to ⬡ Graph View to see the full computation network evolve live.

Visual Design System

Anglo-futurist computational palette:

Role	Colour
Background	#0A0C0F
Surface	#0F1215
Formula Nodes	#1A3A2A
Accent Blue	#1A6EFF
Gold Signal	#C8A84B
Cyan Data Flow	#29C4D8
Primary Text	#E8EDF3
System Identity

Aardvark is not a spreadsheet.

It is a computational ecology for structured thought.

Built with:

Python
PySide6
matplotlib
Claude (Anthropic AI integration layer)
