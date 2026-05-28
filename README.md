# LA-MAQUINARIA-APP-TEMPLATE

Reusable project template for AI-assisted software development. Each project created from this template becomes a self-contained, independently deployable repository.

> Parte del programa **AI First** de [AI Biz School](https://aibizschool.com) — la academia de IA aplicada a negocios de Yami Gala. Inspirado en **Prometeo**, el sistema multi-agente que opera el negocio de Yami 24/7.

## Usage

1. Duplicate this repository for each new project
2. Fill in `START_PROJECT_PROMPT.md` with your project description
3. Run `/init-project` to begin Planning Mode
4. After plan approval, run `/start-execution` to begin implementation

## Structure

- `CLAUDE.md` — AI operating rules and governance
- `planning/` — Requirements, scope, questions, risks
- `design/` — Architecture, data model, API contracts, UI wireframes
- `implementation/` — Task tracker and journey definitions
- `deployment/` — Docker, EasyPanel, deployment scripts
- `docs/` — Project memory, work log, decisions
- `skills/` — Skill registry
- `mcps/` — MCP and API registry
- `backend/` — Backend application code
- `frontend/` — Frontend application code
- `tests/` — Test suites

## Commands

| Command | Purpose |
|---------|---------|
| `/init-project` | Start planning a new project |
| `/start-execution` | Begin implementation after plan approval |
| `/session-start` | Resume work at session start |
| `/review` | Run independent review after milestones |
| `/iterate` | Handle post-delivery changes |

---

*Creado por Yami Gala para los alumnos del programa AI First de AI Biz School.*
