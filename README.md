# Shipquick Enterprise (BMad + SAFe 6.0)

Shipquick is an enterprise-grade agentic framework that combines **BMad Method** (Agent-driven development) with **SAFe 6.0** (Scaled Agile Framework) and **Beads** (Local State Management).

This repository contains:

1.  **Framework Core**: Agents, Workflows, and Templates (`_bmad/`, `.agent/`).
2.  **Installer Source**: The source code for the `shipquick` npm package (`_npm-package/`).

## Quick Start

### For New Users (Install Framework)

Run the installer to set up a new project with Shipquick agents and workflows:

```bash
npx shipquick@latest install
```

This will:

- Ask for your project preferences.
- Install core agents (Analyst, Architect, Dev, QA, etc.).
- Configure VS Code / Cursor / Windsurf integration.
- Set up SAFe hierarchy (Portfolio, Solution, ART, Team).

### For Contributors (Modify Installer)

The installer source code is located in `_npm-package/`.

To build and test the installer locally:

```bash
cd _npm-package
npm install
npm run bundle   # Bundle the framework content into the package
npm link         # Link 'shipquick' command locally for testing
```

Then run:

```bash
shipquick install
```

## Repository Structure

- **`_bmad/`**: Core framework definitions (Agents, Tasks).
- **`.agent/`**: Workflow definitions (Phases 1-5).
- **`_npm-package/`**: Source code for the CLI installer.
- **`.beads/`**: Local state database (for Contributors).
- **`agents.md`**: Agent manifesto and rules.

## State Management (Beads)

Shipquick uses [Beads](https://github.com/StartCompass/beads) for local state management and context tracking.
The installer vendors a pre-built binary of `bd` for seamless cross-platform support.

---

**Maintained by:** CivilEngineersCanAlsoCode
