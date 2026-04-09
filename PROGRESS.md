# autoresearch-mlx Progress

## Status: Forked — Issues Created, No Custom Code Yet

### Completed
- [x] Forked from trevin-creator/autoresearch-mlx
- [x] 9 GitHub issues covering full integration plan
- [x] Original code reviewed: train.py, prepare.py, program.md, results.tsv
- [x] Architecture designed: two-agent loop (researcher + meta-monitor)
- [x] Knowledge base wiki structure designed (researcher + monitor wikis)
- [x] marimo-pair collaboration workflow designed

### The Fork Contains (from upstream)
- train.py — Mutable training script (GPT on MLX, SSSL attention pattern)
- prepare.py — Fixed evaluation harness (val_bpb metric, 5-min budget)
- program.md — Agent protocol (currently references Claude Code)
- results.tsv — Experiment log
- pyproject.toml — MLX dependencies managed by uv

### Next Steps
- [ ] Create agent.py — Replace Claude Code with Gemma 4 as researcher
- [ ] Create monitor.py — Meta-monitor with stuck detection
- [ ] Create notebooks/autoresearch_dashboard.py — marimo dashboard
- [ ] Implement wiki-integrated experiment loop (pre-flight + post-experiment)
- [ ] Integrate newton-mlx kernels for training throughput
- [ ] Docker containerization with MLX GPU passthrough
- [ ] TurboQuant for extended agent context
