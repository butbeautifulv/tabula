# Tabula — AGENTS

Compliance domain umbrella for cxado. First product: **fstec** (FSTEC measures, orders, organizations).

Master plan: [docs/plans/tabula_master.plan.md](docs/plans/tabula_master.plan.md)

## Product path

| Module | Path | Repo |
|--------|------|------|
| FSTEC | `fstec/` | [butbeautifulv/fstec](https://github.com/butbeautifulv/fstec) |

Load fstec-specific rules from the fstec repo when working inside `fstec/`.

## Stack (fstec)

- **Frontend:** Next.js 16, React 19, Tailwind 4, shadcn/ui + `@cxado/gui`
- **Data:** PostgreSQL via Prisma
- **GUI hub:** `shared/gui` in cxado meta-repo (`make gui-link` or `file:../../../shared/gui`)

## Agent workflow

Thin overlay: `.agents/rules/tabula-agent-workflow.mdc` + `make rules-link` from cxado meta-repo.

## Branches

- Tabula umbrella: `tabula/phase-NN-<slug>`
- FSTEC product: `fstec/phase-NN-<slug>` or `fstec/gui-detach-wip` for GUI migration

## Verify (fstec)

```bash
cd fstec
npm run typecheck
npm run lint
npm run build
```
