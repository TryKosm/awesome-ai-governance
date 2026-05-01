# Awesome AI Governance [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of high-quality projects, papers, and primitives for building **governed AI systems** — policy-as-code, approvals, audit trail, supply-chain integrity, observability, workflow orchestration, agent frameworks, and LLM safety research.

This list exists because the AI tooling space is huge and noisy, but the slice that actually matters for production agent systems — *can this action be allowed, who approves it, what was decided, and can we replay it?* — is scattered across dozens of communities. The goal is to keep this list small, opinionated, and useful for engineers building real systems.

Maintained as part of [SomaOS](https://github.com/TryKosm/somaos-docs).


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

