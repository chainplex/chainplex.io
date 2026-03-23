# ChainPlex Build Workflow

## Agent Roles

| Agent | Role | Tool |
|-------|------|------|
| **Veera** | Orchestrator — writes specs, delegates, reviews, approves deploys | Main session |
| **Builder** | Receives task spec, builds features, reports back | Claude Code CLI |
| **QA** | Reviews code, checks for bugs/issues, approves or requests fixes | Subagent |

## Pipeline

```
Thiyaghu → Veera (spec) → Builder (build) → QA (review) → Veera (approve) → Deploy
```

## Deploy Command
```bash
cd /Users/thiyaghu/.openclaw/workspace/projects/btc-dashboard
git add -A && git commit -m "<message>" && git push https://x-access-token:$(gh auth token)@github.com/chainplex/chainplex.io.git main
```
