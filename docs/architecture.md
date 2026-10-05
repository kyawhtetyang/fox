# Fox Architecture

Fox is a headless, capability-first runtime kernel with clear boundaries. It is not a second Personal OS: Personal OS owns semantic knowledge, governance, current State, and canonical automation capability discovery.

```text
HUMAN / AI / CLI / FUTURE API
             |
             v
        Access Layer
             |
             v
       Context Layer
             |
             v
Capabilities / Discovery / State / Artifacts
             |
             v
      Execution Engine
             |
             v
          Runtime
             |
             v
           Data
```

## Layers

- vault/ contains local fixtures and sandbox material only; it is not the Personal OS human workspace.
- system/ contains kernel-local rules, contracts, capabilities, and discovery metadata; it is not Personal OS governance.
- runtime/ contains executable system behavior.
- data/ contains local runtime status, artifacts, and run records. It cannot establish Personal OS current truth.
- context/ selects and projects relevant information without depending on an AI provider.

## Canonical execution

```text
Client
  ↓
ExecutionRequest
  ↓
ExecutionEngine
  ↓
Capability
  ↓
Verification
  ↓
Run + Artifact + State
  ↓
Canonical Result
```

## Access Layer

The generic CLI command is the canonical execution access path:

```bash
python -m runtime execute <capability> --input '<json>' --options '<json>'
```

Specialized commands such as `media save` remain convenience adapters. They translate user-friendly arguments into canonical request models and use the same ExecutionEngine lifecycle.

The Access Layer does not introduce a new router, planner, orchestrator, or execution model.

## Personal OS Boundary

This repository neither reads from nor writes to the Personal OS repository. Its capability registry lists only kernel-local capabilities and is not a replacement for Personal Automation's canonical registry. Any future exchange must be introduced through an explicit, versioned integration contract that names the source of truth and the permitted direction of data flow.

## Context

```text
Consumer
  ↓
ContextRequest
  ↓
ContextAssembler
  ↓
Sources
  ↓
Canonical Context
  ↓
Projection
```

Context is not a knowledge store, prompt, or model adapter.
