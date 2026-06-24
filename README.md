# CNS Munich 2026 — Why LLMs Get Expensive in Production

Resources from my talk at **[Cloud Native Summit Munich 2026](https://cloudnativesummit.de/)** (June 29–30, Munich): **why LLMs become expensive in production, and how a control-plane architecture fixes it.**

🔗 **Live page:** https://hiranyakavishani.github.io/cns-munich-2026/

---

## The argument, in one line

The cost isn't the model — it's the non-deterministic loops, ungoverned traffic, and missing observability around it. The fix is a control plane: make the work deterministic, govern and route it, then scale that pattern across many agents. Each resource below maps to one step.

### Step 1 · Make the work deterministic
- **[Arazzo → MCP Tool (CLI Quick Start)](https://wso2.com/api-platform/docs/tools/arazzo-mcp-gen-cli/quick-start-guide/)** — design business tasks as deterministic Arazzo workflows, then wrap them as a single MCP tool. The agent loop calls one tool instead of burning tokens improvising the whole sequence.

### Step 2 · Govern & route the traffic
- **[WSO2 AI Gateway](https://wso2.com/api-platform/ai-gateway/)** — rate limits, token budgets, and routing at the edge, where runaway LLM cost is contained.
- **[AI Workspace](https://wso2.com/api-platform/ai-workspace/)** — the control plane: set policy, see cost and usage before it's a bill.

### Step 3 · Scale it across many agents
- **[WSO2 Agent Manager & Agent ID](https://wso2.com/about/news/wso2-launches-agent-manager/)** — the same pattern extended to a fleet, with identity and lifecycle for every agent.

### More
- 📊 **[Slides](https://hiranyakavishani.github.io/cns-munich-2026/slides.pdf)**
- 💬 **[Connect on LinkedIn](https://www.linkedin.com/in/hiranya-kavishani/)** · hiranyaa@wso2.com

---

## Running locally

Single static file — no build step:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying

GitHub Pages: **Settings → Pages → Source: `main` branch / root**.

---

Built for the cloud native community by **Hiranya Abeyrathne**. Questions about AI gateways, agents, and keeping LLM cost under control? Find me on [LinkedIn](https://www.linkedin.com/in/hiranya-kavishani/) or email hiranyaa@wso2.com.
