# LangGraph Cookbook

Practical LangGraph agent examples built with Claude (Anthropic). Each notebook is a self-contained recipe covering a different tool or use case.

## Recipes

| # | Notebook | Topic |
|---|---|---|
| 01 | `01_intro_basics.ipynb` | LangGraph fundamentals — nodes, edges, graph compilation |
| 02 | `02_chatbot_tavily_search.ipynb` | Conversational chatbot with Tavily web search tool |
| 03 | `03_stock_ticker_agent.ipynb` | Stock ticker agent with tvscreener API |
| 04 | `04_stock_info_claude.ipynb` | Stock info agent powered by Claude + tvscreener |
| 05 | `05_haiku_generator.ipynb` | Haiku generator with tool calling (Claude Sonnet + Haiku) |
| 06 | `06_gsea_proteomics.ipynb` | Gene set enrichment analysis with gseapy and CPTAC proteomics data |
| 07 | `07_langgraph_gsea_tool.ipynb` | LangGraph agent wrapping gseapy enrichr for pathway analysis |

---

## Installation

### Step 1 — Create a clean environment

```bash
conda create -n langgraph-cookbook python=3.11 -y
conda activate langgraph-cookbook
```

### Step 2 — Install dependencies

```bash
pip install -r requirements.txt
```

### Step 3 — Configure your API key

```bash
cp .env.example .env      # Mac/Linux
copy .env.example .env    # Windows
```

Edit `.env`:

```
ANTHROPIC_API_KEY=sk-ant-...
TAVILY_API_KEY=tvly-...   # required for notebook 02
```

### Step 4 — Launch Jupyter

```bash
jupyter notebook
```

---

## Tech stack

| Layer | Library |
|---|---|
| Agent framework | [LangGraph](https://github.com/langchain-ai/langgraph) |
| LLM | Anthropic Claude via `langchain-anthropic` |
| Web search | Tavily (`tavily-python`) |
| Stock data | `tvscreener` |
| Bioinformatics | `gseapy` |
| Notebook | Jupyter |
