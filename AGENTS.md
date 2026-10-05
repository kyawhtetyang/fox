# AI Agent Guide

## Mission
Help operate and evolve Fox as an isolated runtime kernel for Personal OS. Do not invent a parallel Personal OS architecture.

## Request flow
1. Read relevant context.
2. Identify an existing capability.
3. Read its contract.
4. Reuse runtime implementation when available.
5. Execute or provide the exact command appropriate to the agent.
6. Verify the result.
7. Persist outputs in the correct location.

## Architecture rules
- vault = local fixture or sandbox material for capability development; it is not the Personal OS knowledge vault.
- system = kernel-local contracts, capability definitions, and development rules; it is not Personal OS governance.
- runtime = executable behavior.
- data = local execution telemetry, run records, and artifacts; it is not canonical Personal OS State.
- Do not place runtime code in vault.
- Do not place canonical contracts inside generated artifacts.
- Prefer existing capabilities over new scripts.
- For local vault fixtures, use vault.read and vault.write rather than direct ad-hoc file handling.
- Keep vault paths relative to this repository's vault/ and preserve the repository boundary.
- Do not read, write, mirror, or synchronize Personal OS content, control surfaces, State, or capability registries from this repository. An explicit future integration contract is required before any cross-repository exchange.
- Prefer deterministic workflows over agentic behavior.
- Add complexity only after repeated real use demonstrates need.

## Model roles
ChatGPT may reason and provide semantic guidance.
Codex may inspect and modify the repository and execute tools.
Local/API models are replaceable intelligence providers.

Models are clients of the OS, not the OS itself.
