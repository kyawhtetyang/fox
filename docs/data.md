# Data Layer

## Purpose

The data layer preserves local machine-facing execution telemetry. It is not a source of Personal OS semantic truth or current State.

## Structure

- state/ — current machine-readable state
- artifacts/ — generated outputs
- runs/ — execution records

Flow:

REQUEST
→ EXECUTE
→ VERIFY
→ ARTIFACT
→ RUN RECORD

Run records allow humans and AI models to inspect execution history without depending on chat history.
