# CLAUDE.md

**Keep directives terse.** State the rule in one sentence. Add *why* only if non-obvious. Skip examples unless the rule is ambiguous without one.

## Project overview

Flux GitOps repo with the standard `apps/` (base + per-cluster overlays) and `clusters/` (per-cluster Flux bootstrap) layout. Workloads (podinfo, nginx, hpa-workload) live in `apps/base/`; clusters (kind-cluster-1, kind-reid-1) consume them via Kustomize overlays.

Primary use right now: evaluating Flux's field-management and drift-handling behaviors. Treat scratch changes under `apps/base/podinfo` and `apps/kind-cluster-1` as evaluation scaffolding, not production config.

