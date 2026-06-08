# Awesome Ai Governance

Curated list for policy-as-code, audit, agents, and LLM safety.

This list exists because the AI tooling space is huge and noisy, but the slice that actually matters for production agent systems — *can this action be allowed, who approves it, what was decided, and can we replay it?* — is scattered across dozens of communities. The goal is to keep this list small, opinionated, and useful for engineers building real systems.

Part of the [TryKosm](https://github.com/TryKosm) open-source collection.


## Contents

- [Policy engines](#policy-engines)
- [Audit & supply-chain integrity](#audit--supply-chain-integrity)
- [Observability for AI](#observability-for-ai)
- [Workflow orchestration](#workflow-orchestration)
- [Agent frameworks](#agent-frameworks)
- [LLM safety & red-teaming](#llm-safety--red-teaming)
- [Contributing](#contributing)


## Policy engines

Policy-as-code: encode "what is allowed" once, evaluate it consistently from any service.

- [open-policy-agent/opa](https://github.com/open-policy-agent/opa) — General-purpose policy engine. The de facto standard for cloud-native authorization.
- [cerbos/cerbos](https://github.com/cerbos/cerbos) — Stateless authorization service with human-readable policies and good developer ergonomics.
- [casbin/casbin](https://github.com/casbin/casbin) — Multi-language access control library supporting RBAC, ABAC, and more.
- [kyverno/kyverno](https://github.com/kyverno/kyverno) — Kubernetes-native policy engine; useful pattern for declarative policy lifecycles.
- [openfga/openfga](https://github.com/openfga/openfga) — Relationship-based access control inspired by Google Zanzibar.
- [authzed/spicedb](https://github.com/authzed/spicedb) — High-performance Zanzibar-style permissions database.
- [ory/keto](https://github.com/ory/keto) — Open-source implementation of Google's Zanzibar.
- [permitio/permit-python](https://github.com/permitio/permit-python) — Permit.io Python SDK for attribute-based access control in backend services.


## Audit & supply-chain integrity

Tamper-evident logs and provenance you can actually defend in an audit.

- [sigstore/cosign](https://github.com/sigstore/cosign) — Container signing, verification, and storage in an OCI registry. The reference for software signing.
- [in-toto/in-toto](https://github.com/in-toto/in-toto) — Framework for securing the integrity of software supply chains.
- [slsa-framework/slsa](https://github.com/slsa-framework/slsa) — Supply-chain Levels for Software Artifacts: a security framework with progressive levels.
- [tektoncd/chains](https://github.com/tektoncd/chains) — Build provenance and signed metadata for Tekton pipelines.
- [guacsec/guac](https://github.com/guacsec/guac) — Aggregates and queries software supply-chain metadata.
- [transparency-dev/trillian](https://github.com/transparency-dev/trillian) — Transparent, append-only log infrastructure.
- [TWZRD Agent Intel](https://intel.twzrd.xyz) — On-chain agent wallet trust scoring on Solana. Query verifiable reputation history, behavioral risk flags, and transaction patterns for autonomous agent identities. Issues signed trust receipts (on-chain) via x402 micropayments. MCP endpoint at `https://intel.twzrd.xyz/mcp`.


## Observability for AI

Tracing, metrics, and event pipelines you can route AI workflow telemetry through.

- [open-telemetry/opentelemetry-collector](https://github.com/open-telemetry/opentelemetry-collector) — Vendor-neutral telemetry pipeline. Use it as the gateway for traces, metrics, logs.
- [vectordotdev/vector](https://github.com/vectordotdev/vector) — High-performance observability data pipeline. Excellent for shaping audit / event streams.
- [prometheus/prometheus](https://github.com/prometheus/prometheus) — Time-series metrics. The default for SLO-backed AI service dashboards.
- [grafana/grafana](https://github.com/grafana/grafana) — Visualization layer for metrics, traces, and logs.
- [grafana/loki](https://github.com/grafana/loki) — Log aggregation system; pairs well with Grafana for audit drilldown.
- [Arize-ai/phoenix](https://github.com/Arize-ai/phoenix) — Open-source LLM observability with traces and evals.
- [traceloop/openllmetry](https://github.com/traceloop/openllmetry) — OpenTelemetry instrumentation for LLM applications.


## Workflow orchestration

When agent flows get past the chat-loop stage, you need durable execution.

- [temporalio/temporal](https://github.com/temporalio/temporal) — Durable execution platform. The de facto choice for long-running agent workflows.
- [cadence-workflow/cadence](https://github.com/cadence-workflow/cadence) — Uber's fault-tolerant orchestrator; sibling project to Temporal.
- [argoproj/argo-workflows](https://github.com/argoproj/argo-workflows) — Kubernetes-native workflow engine. Strong for ML/AI pipelines.
- [dagger/dagger](https://github.com/dagger/dagger) — Programmable CI/CD and pipeline engine; useful for governed build pipelines around AI services.
- [kedacore/keda](https://github.com/kedacore/keda) — Event-driven autoscaling for Kubernetes; pairs with workflow engines for bursty agent loads.
- [apache/airflow](https://github.com/apache/airflow) — Mature DAG orchestrator; widely used for governed batch AI pipelines.
- [PrefectHQ/prefect](https://github.com/PrefectHQ/prefect) — Modern Python-native workflow orchestrator.


## Agent frameworks

Where the requesters of governed actions actually come from.

- [langchain-ai/langchain](https://github.com/langchain-ai/langchain) — Most-adopted agent / LLM framework. Wide ecosystem.
- [run-llama/llama_index](https://github.com/run-llama/llama_index) — Data framework for LLM applications. Strong RAG primitives.
- [microsoft/autogen](https://github.com/microsoft/autogen) — Multi-agent conversation framework from Microsoft Research.
- [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) — Role-based multi-agent orchestration.
- [stanfordnlp/dspy](https://github.com/stanfordnlp/dspy) — Programming with foundation models, with optimization over prompts.
- [langgenius/dify](https://github.com/langgenius/dify) — Visual LLM app development platform.
- [Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) — Original autonomous agent project; useful as a reference design point.


## LLM safety & red-teaming

The empirical side of "what can go wrong" — required reading before you trust an agent with policy.

- [leondz/garak](https://github.com/leondz/garak) — LLM vulnerability scanner. Probes for hallucination, prompt injection, leakage, etc.
- [protectai/llm-guard](https://github.com/protectai/llm-guard) — Comprehensive LLM input/output security toolkit.
- [NVIDIA/NeMo-Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) — Programmable guardrails for conversational LLM applications.
- [guardrails-ai/guardrails](https://github.com/guardrails-ai/guardrails) — Python framework for adding validation and structure to LLM outputs.
- [confident-ai/deepeval](https://github.com/confident-ai/deepeval) — Evaluation framework for LLM applications, including safety metrics.
- [openai/evals](https://github.com/openai/evals) — Framework and registry of benchmarks for evaluating LLM behavior.
- [EleutherAI/lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) — Standard harness for LM evaluation across tasks.
- **Papers:** [Universal and Transferable Adversarial Attacks on Aligned LLMs (Zou et al., 2023)](https://arxiv.org/abs/2307.15043), [Prompt Injection attack against LLM-integrated Applications (Liu et al., 2023)](https://arxiv.org/abs/2306.05499), [Constitutional AI (Anthropic, 2022)](https://arxiv.org/abs/2212.08073).


## Contributing

Contributions are welcome. Before opening a PR:

1. Make sure the project has been actively maintained in the last 12 months.
2. Make sure the entry is more than a wrapper around an existing entry on this list.
3. Keep the description to one line, focused on **what it does** and **why it belongs in a governance/AI-infra context**.
4. Add the entry to the most relevant section, alphabetized within reason.

Open a PR with the addition and a short note on why it qualifies. PRs that add affiliate links, vendor-only solutions without a real OSS surface, or duplicates will be closed.

## License

This curated list is licensed under the MIT License — see [`LICENSE`](LICENSE).
