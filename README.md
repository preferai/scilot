# Scilot

An open-source exploration-exploitation layer for autonomous ML research loops.

![Scilot Architecture](scilot_architecture.png)

## What is Scilot?

Scilot is a model-agnostic agent harness that adds structured exploration infrastructure on top of existing autoresearch loops (e.g., Karpathy's [autoresearch](https://github.com/karpathy/autoresearch)). Where current approaches are greedy hill-climbers with no structured exploration, Scilot introduces:

- **Autoresearch Ledger Schema** — open interoperability format for structured experiment tracking (CC0)
- **Hypothesis Taxonomy** — versioned classification of ML hypothesis families (CC0)
- **Exploration policy** — bandit-based strategies (Thompson sampling, Gaussian process surrogate) to select which hypothesis families to pursue next, informed by live metric feedback from executed experiments
- **Backend comparison study** — empirical evaluation of local open-source models (Ollama) vs. commercial APIs as autoresearch backends

## Motivation

Existing autoresearch strategies propose, implement, and evaluate changes via a git-based ratchet but have no structured exploration. They treat all hypothesis families equally and produce no reusable experiment record. Scilot sits on top of the open agent ecosystem and adds the exploration infrastructure that is missing.

## Status

Under development. Funded by [NGI Zero Commons Fund](https://nlnet.nl/commonsfund/) (NLnet Foundation, 13th round).

## Planned outputs (Apache 2.0 / CC0)

- Agent harness with pluggable exploration policies
- Autoresearch Ledger Schema v1.0 (JSON Schema + CLI)
- Hypothesis Taxonomy v1.0 (YAML)
- Four-backend comparison study arXiv preprint
- Scilot v1.0 on PyPI

## Team

[Prefer AI d.o.o.](https://preferai.hr) — Dr. Emanuel Lacic & Tomislav Duricic

## License

Apache 2.0 (code) · CC0 (schemas and taxonomy)
