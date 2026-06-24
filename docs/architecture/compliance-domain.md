# Compliance domain (Tabula)

Tabula groups compliance-oriented products under cxado. It is an umbrella repo, not a runtime monolith — each product keeps its own git lifecycle and deploy.

## Boundaries

| Layer | Owner | Notes |
|-------|-------|-------|
| Domain logic | Product repos (fstec) | Prisma models, API routes, business rules |
| Shared UI | `shared/gui` (`@cxado/gui`) | Tiers 1–3 primitives, dashboard shells |
| Agent rules | `shared/agent-rules` + thin overlay | `make rules-link` from cxado |
| Contracts | `shared/contracts/` (planned) | Cross-domain events |

## fstec (first module)

FSTEC regulatory measures tracking: organizations, orders, measures, public dashboards, corpus import.

Three-context Next.js layout:

- `(public)/` — tokenized dashboards
- `(platform)/` or admin — operator UI
- `api/` — route handlers

Public routes must not import platform-only modules.

## Relationship to cxado

```
cxado (meta-repo)
  projects/tabula/     ← submodule (this repo)
    fstec/             ← submodule (fstec product)
  shared/gui/          ← @cxado/gui hub
```

## GUI strangler

FSTEC migrates in-repo UI to `@cxado/gui` via re-export shims under `@/components/ui/*`. Domain-specific presentation stays in `lib/cxado-gui/fstec-adapter.ts` and dashboard wrappers.
