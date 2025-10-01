# Multi-Agent Investment Analysis System

AI-powered stock analysis system using CrewAI's multi-agent framework with autonomous task delegation and real-time data integration.

## Overview

Four specialized AI agents collaborate to analyze stocks: Portfolio Manager (coordinates team), Market Analyst (scrapes financial news), Research Analyst (analyzes documents with RAG), and Trading Strategist (generates recommendations).

## Features

- **Agent Delegation**: Portfolio Manager automatically assigns tasks to specialists
- **RAG Integration**: Analyzes uploaded financial documents (earnings reports, SEC filings)
- **Real-Time Data**: Live market data via yFinance + web scraping
- **Custom Tools**: Risk/reward calculator, technical indicators (SMA, RSI), fundamental metrics
- **Structured Output**: Entry/exit points, tiered targets, stop-loss levels, position sizing

## Tech Stack

- CrewAI, LangChain, OpenAI GPT-4 Mini
- yFinance, Python 3.8+
- RAG (FileReadTool), custom financial calculators

## Installation
```bash
pip install crewai crewai-tools langchain-openai yfinance plotly
export OPENAI_API_KEY='your-api-key-here'

## Usage
# Analyze a stock
result = analyze_stock('AAPL')

# Enhanced analysis with custom tools
result = enhanced_analyze_stock('NVDA')
Example Results

TSLA: SELL at $322 | Targets: $300, $280, $250 | Risk/Reward: 3:1
GOOGL: BUY at $173 | Targets: $180, $185, $190 | Risk/Reward: 2.5:1
NVDA: BUY at $145 | Targets: $160, $180, $200 | Risk/Reward: 4:1
