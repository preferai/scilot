# Scilot

An exploration-exploitation framework for autonomous ML research loops.


## What is Scilot?

Scilot generalizes the problem to autonomous AI research (i.e., inspired by Karpathy's [autoresearch](https://github.com/karpathy/autoresearch) for LLMs) for diverse ML models. It adds structured exploration and is model-agnostic when conducting agentic research. The architecture has four zones:

- **Zone 1 — Autoresearch Inner Loop (existing):** the standard ratchet loop — propose hypothesis → implement change → evaluate metric → accept/revert — via a git-based ratchet.
- **Zone 2 — Open Agent Harness:** model-agnostic harness supporting both local open-source models (Llama, Qwen, etc.) and commercial ones.
- **Zone 3 — Policy Layer:** a Hypothesis Classifier and Surrogate Model feed an Exploration Policy that sends AI model family recommendations back into the loop. All experiments are recorded in a Structured Experiment Ledger.
- **Zone 4 — Open Artifacts:** the Autoresearch Ledger Schema and Hypothesis Taxonomy are published as open interoperability artifacts.

![Scilot Architecture](scilot_architecture.png)


## Motivation

Existing autoresearch strategies treat all hypothesis families equally and produce no reusable experiment record. Scilot adds the exploration infrastructure that is missing: principled hypothesis selection, a surrogate model trained on past runs, and open schemas that make experiment records portable across tools and teams.

## Status

Under development. Funded by [NGI Zero Commons Fund](https://nlnet.nl/commonsfund/) (NLnet Foundation, 13th round).
