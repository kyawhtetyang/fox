# Fox

Fox is an isolated, capability-first runtime kernel for Personal OS. Personal OS remains the canonical human-and-AI operating system.

It owns only its local runtime behavior, contracts, test fixtures, and execution telemetry. It does not own Personal OS knowledge, governance, current State, or automation capability discovery.

## Core flow

Human / AI / CLI
→ Context
→ Capability
→ Runtime
→ Verification
→ Data

## Architecture

- vault/ — Local capability fixtures and sandbox material
- system/ — Kernel-local contracts and capability definitions
- runtime/ — Execution implementations and canonical runtime behavior
- data/ — Local runtime status, artifacts and run records
- ops/ — Maintenance
- tests/ — Quality
- docs/ — Architecture and documentation
- archive/ — Historical material

## Principle

Start deterministic and simple. Add workflows when repeated. Add dedicated orchestration only when real coordination problems justify it.

## Canonical execution

```bash
python -m runtime execute media.save \
  --input '{"url":"https://example.com/video"}' \
  --options '{"mode":"audio"}'
```

Local vault-fixture access is Markdown-first through `vault.read` and `vault.write`. Human-friendly capability commands remain available as convenience adapters.

Status: v0.6.0 Vault Access Foundation.
