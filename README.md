# TradePilot AI — Binance Agent OS Mini Hackathon (Track A)

**AI-powered trading workflow agent built natively on Binance Agent OS + MCP**

🏆 Submission for the **Binance Agent OS Mini Hackathon**  
Track A: Build an AI agent with Agent OS ($20,000 USDC prize pool)

---

## What is TradePilot AI?

TradePilot is a production-ready AI agent that turns any compatible LLM (Claude, ChatGPT, Cursor, Codex, etc.) into a full **crypto trading copilot** using the official **Binance MCP Server**.

It covers the four official Agent Workflows highlighted by Binance:

| Workflow              | What TradePilot does                                      |
|-----------------------|-----------------------------------------------------------|
| **Data & Analysis**   | Live market data, SMA/EMA, trend, volatility, risk score  |
| **Trading Workflows** | Signals, strategy suggestions, position sizing, SL/TP     |
| **Payment Workflows** | Ready for agent-to-agent & automated payments (x402)      |
| **Onchain Workflows** | Portfolio insights + on-chain readiness (via Agentic Wallet) |

The agent is **safe by design**:
- Works inside Binance **Agentic sub-accounts** only
- No withdrawal permissions
- Risk limits and confirmation gates
- Dry-run mode by default

---

## Quick Demo (30 seconds)

Once you have the Binance MCP connected:

```
Analyze BTCUSDT with TradePilot. Give me:
1. Current price + 24h change
2. SMA20 / SMA50 trend
3. Volatility score
4. Risk summary
5. Suggested trade idea with position size (risk 1% of wallet)
```

Or simply:

```
Use TradePilot to scan the top movers and give me 3 high-probability setups for the next 4 hours.
```

---

## How to Connect (Official Binance Agent OS)

### 1. Add the official Binance MCP Server

**Claude Code / Claude Desktop:**
```bash
claude mcp add binance-mcp-server --transport http https://agent.binance.com/mcp/agentic
```

Then run `/mcp` → select `binance-mcp-server` → **Authenticate** → grant Market Data + Account + Trade (as needed).

**ChatGPT / Cursor / other clients:**  
Add custom connector → URL: `https://agent.binance.com/mcp/agentic`

### 2. Fund an Agentic sub-account
Profile → Sub-accounts → Asset Management → Transfer (only funds you are willing to risk with the agent).

### 3. Load TradePilot skill / prompts
Copy the content from `/prompts/tradepilot-system.md` into your system prompt or create a Claude Skill / Custom GPT.

---

## Project Structure

```
binance-agentos-tradepilot/
├── README.md
├── LICENSE
├── prompts/
│   ├── tradepilot-system.md          # Main system prompt / skill
│   ├── analysis-workflow.md
│   ├── trading-workflow.md
│   └── risk-rules.md
├── src/
│   ├── tradepilot.py                 # Optional Python helper (demo)
│   └── config.example.yaml
├── docs/
│   ├── architecture.md
│   └── submission.md
└── demo/
    └── example-outputs.md            # Real example responses
```

---

## Key Features

- **Deterministic + AI hybrid** — Technical indicators first, then LLM reasoning
- **Risk-first design** — Position sizing based on % risk, mandatory SL/TP suggestions
- **Multi-timeframe analysis**
- **Portfolio-aware** — Checks current balances and open positions before suggesting size
- **Fully MCP-native** — No custom API keys needed (uses official Binance Agent OS)
- **Works with** Claude, ChatGPT, Cursor, Codex, Grok, any MCP client

---

## Submission Details (Hackathon)

- **Track**: A — Build an AI agent with Agent OS
- **Deadline**: September 8, 2026, 23:59 UTC
- **Required steps**:
  1. Follow @Binance and repost the official post
  2. Reply / Quote with this GitHub + short demo video
  3. Complete the official survey

---

## Disclaimer

This is a hackathon project for educational and demonstration purposes.  
Cryptocurrency trading involves substantial risk of loss.  
TradePilot is not financial advice. Always do your own research and never risk more than you can afford to lose.  
Not available in restricted jurisdictions (US, UK, EEA, HK, SG, etc.).

---

Built with ❤️ for the Binance Agent OS ecosystem.

**We built Agent OS. You build what's next.** 🫡
