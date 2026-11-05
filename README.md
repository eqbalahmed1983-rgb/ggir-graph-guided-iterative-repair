# GGIR — Graph-Guided Iterative Repair

**A research artifact for repository-level software engineering with Gemma 4.**

This repository contains the source code, agent configuration, prompts, repository-navigation and test-discovery skills, supporting scripts, tests, and technical documentation associated with the GGIR research project.

## What is included

- `src/g4agent/`: repository analysis, graph/navigation utilities, experiment and validation support.
- `skills/`: repository navigation, test discovery, and debugging workflows.
- `prompts/` and `sub_agents/`: agent instructions and specialist configurations.
- `agent.yaml`, `configs/`, `eval_config.yaml`: declarative agent and runtime configuration.
- `scripts/`: setup, validation, packaging, and evaluation helpers.
- `tests/`: automated tests for the supporting code.
- `variants/`: documented configuration variants and ablation candidates.
- `docs/`: architecture, methodology, budget, evaluation, and reproducibility notes.

## Important evaluation status

This artifact must not be interpreted as evidence of a measured real-Gemma-4 repair success rate.

- The project documentation reports successful validation/compilation with the competition's official harness and an end-to-end scripted-model pipeline check.
- The scripted-model check validates the tool/harness integration; it is **not** a real Gemma 4 model evaluation.
- The documented real-Gemma-4 evaluation attempt was blocked before any task ran. No real-model resolution rate is reported.
- The documentation reports no Kaggle leaderboard submission or leaderboard score for this project.
- The repository-navigation benchmark described in the documentation is a limited localization experiment; its lexical-proxy/AST limitations are documented and it should not be presented as a competition score.

Please consult `docs/real_baseline.md`, `docs/experiments.md`, and `docs/final_submission_audit.md` before interpreting any reported checks or measurements.

## Reproducibility

The documented local workflow is:

```bash
scripts/setup.sh
scripts/setup_official_harness.sh
scripts/validate.sh
scripts/package_submission.sh
```

These commands may require a compatible Python environment and the dependencies listed in `requirements.txt` / `pyproject.toml`. Real-model evaluation requires the official competition environment, access credentials, and the specified Gemma 4 serving stack. Do not substitute a different model and describe it as an official Gemma 4 run.

## Relationship to the paper

GGIR is the research framing for combining repository-aware retrieval, structural navigation, evidence-driven repair, and test-guided iteration. The exact implemented configuration and the status of optional specialist agents are described in `agent.yaml`, `variants/`, and `docs/architecture.md`. The paper should distinguish the currently validated single-agent configuration from optional or experimental multi-agent variants.

## Scope and exclusions

This public research-artifact bundle intentionally excludes raw task/evaluation datasets, raw run traces, cached leaderboard data, and machine-specific evaluation output directories. It is a source-and-documentation artifact, not a claim that a real-model benchmark has been completed.
