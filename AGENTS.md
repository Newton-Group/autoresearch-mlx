# autoresearch-mlx — Agent Index

## Repo Purpose
Autonomous ML research loop: Gemma 4 agent edits train.py, runs 5-min experiments, measures val_bpb, keeps or reverts. Fork of Karpathy's autoresearch ported to MLX.

## Critical Files
| File | Purpose | Mutable? |
|------|---------|----------|
| train.py | Model architecture + training loop | YES — this is what the agent edits |
| prepare.py | Evaluation harness, data loading, tokenizer | NO — read-only |
| program.md | Agent protocol (experiment rules) | Reference only |
| results.tsv | Experiment log (commit, val_bpb, memory, status) | Append-only |
| pyproject.toml | Dependencies (mlx, numpy, pyarrow, tiktoken) | Rarely |

## Key Metrics
- val_bpb — validation bits-per-byte (lower is better)
- Best so far: 1.353329 (46 steps in 312s training)
- Fixed 5-minute training budget — faster kernels = more steps = lower val_bpb

## Files To Be Created
| File | Purpose |
|------|---------|
| agent.py | Gemma 4 research agent (replaces Claude Code) |
| monitor.py | Meta-monitor for stuck detection |
| notebooks/autoresearch_dashboard.py | marimo dashboard |
| notebooks/experiment_workbench.py | Human-agent collaboration notebook |

## Architecture Reference
See `Newton-Group/newton-design/DESIGN.md` Section 5 for canonical models.
See issues #1-#9 for full implementation plan.
