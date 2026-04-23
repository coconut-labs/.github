# coconut labs

Small systems lab. LLM infra + market systems.

### [kvwarden](https://github.com/coconut-labs/kvwarden)
Tenant-fair LLM inference orchestration on a single GPU. No Kubernetes. Token-bucket fairness sits in front of vLLM so one tenant's flood doesn't starve the others.

Measured on A100 + vLLM 0.19.1 under a 32 RPS flooder:
- FIFO baseline: **1,585 ms** p99 (29× starvation)
- kvwarden: **61.5 ms** p99 (1.14× solo)

Fills the gap between Ollama (single-user) and Dynamo / llm-d (datacenter).

```
pip install kvwarden
```

### Minerva
NSE stage-analysis screener. Minervini SEPA rules on Indian equities — VCP detection, IBD-weighted RS percentile, 7-level exit hierarchy, walk-forward backtesting. Private while it bakes.

---

Built by [@ShreyPatel4](https://github.com/ShreyPatel4).
Co-Built by [@jaypatel15406](https://github.com/jaypatel15406).
