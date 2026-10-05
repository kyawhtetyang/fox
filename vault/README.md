# Vault

Local capability-fixture and sandbox workspace.

It may be opened in Obsidian for development, but it is not a Personal OS knowledge vault and must not become a mirror of Personal OS notes, journals, projects, or knowledge.

## Canonical access

Vault access is Markdown-first and capability-based:

- `vault.read` — read one Markdown file using a path relative to `vault/`.
- `vault.write` — write one verified Markdown file using a path relative to `vault/`.

Paths cannot escape this repository's vault/ boundary. Existing files are not overwritten unless explicitly requested.

Runtime code, machine state, and generated artifacts should not be mixed into the vault by default.
