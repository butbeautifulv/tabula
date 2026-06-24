# Tabula — master plan

## Overview

Compliance domain for cxado. fstec is the first product module; future modules may share `shared/contracts/` event schemas.

## Phase status

| Phase | Branch | Status |
|-------|--------|--------|
| 00-scaffold | tabula/phase-00-scaffold | done |
| 01-fstec-submodule | tabula/phase-01-fstec-submodule | done |
| 02-gui-hub | fstec/gui-detach-wip | in progress |
| 03-contracts | tabula/phase-03-contracts | planned |

## Module map

| Module | Repo | Role |
|--------|------|------|
| fstec | `fstec/` submodule | FSTEC measures, orders, org dashboard |

## GUI hub (phase 02)

1. Pin `@cxado/gui` from cxado `shared/gui` (not sibling `cxado-gui`)
2. `globals.css` → `@import "@cxado/gui/tailwind.preset.css"`
3. Dashboard hybrid tables: FSTEC wrappers over `@cxado/gui` primitives
4. Green `npm run build` on WIP; **do not merge fstec master** until critic + CI

## Contracts (phase 03 — later)

Optional compliance event schemas in cxado `shared/contracts/` for egregore/veil integration.

## Resume / next

1. Complete `fstec/gui-detach-wip` with `shared/gui`
2. Merge fstec WIP → master after Tabula + CI sign-off
3. hexenhammer phase 05 (`@cxado/gui` tier-1) unblocked after fstec GUI stabilizes
