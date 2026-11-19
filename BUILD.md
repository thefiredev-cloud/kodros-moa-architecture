# Build guide: kodros-moa-architecture

This repository is documentation. There is no program to build.

## Read it

Open the repository on GitHub. The Mermaid diagrams in `README.md` and `docs/ARCHITECTURE.md` render in the browser. In an editor that does not render Mermaid, use [docs/architecture.svg](docs/architecture.svg) for the summary diagram.

```bash
git clone https://github.com/thefiredev-cloud/kodros-moa-architecture.git
cd kodros-moa-architecture
```

## Redraw the static diagram

You need Graphviz (`dot`). On Debian or Ubuntu: `sudo apt install graphviz`. On macOS: `brew install graphviz`.

```bash
dot -Tsvg docs/architecture.dot -o docs/architecture.svg
```

Edit `docs/architecture.dot` first if the structure changes. Keep the README Mermaid block in step with it.

## Check the Mermaid blocks

Paste a block into the [Mermaid live editor](https://mermaid.live), or render it with `@mermaid-js/mermaid-cli` (`npx @mermaid-js/mermaid-cli -i input.mmd -o out.svg`). The `mmdc` route needs a headless Chromium.

## What to expect

Only the MoA loop is implemented, in [Hermes Agent](https://github.com/NousResearch/hermes-agent). Roles, approval levels, the vault and the audit trail are design intent. [README.md](README.md) has the status table.
