# Tabula — compliance domain

Tabula is the **compliance** domain umbrella for [cxado](https://github.com/butbeautifulv/cxado). [fstec](https://github.com/butbeautifulv/fstec) is the first product module: FSTEC measures, orders, organizations, and reporting.

## Layout

```
tabula/
  fstec/          # submodule → butbeautifulv/fstec
  docs/
  .agents/rules/  # thin agent overlay (core rules via cxado make rules-link)
```

## Status

| Phase | Item | State |
|-------|------|-------|
| 00 | Tabula scaffold (this repo) | done |
| 01 | fstec submodule | done |
| 02 | GUI hub via `shared/gui` | in progress on `fstec/gui-detach-wip` |
| 03 | Compliance contracts → `shared/contracts/` | planned |

## Bootstrap (from cxado meta-repo)

```bash
git clone --recurse-submodules https://github.com/butbeautifulv/cxado.git
cd cxado && make bootstrap
# projects/tabula/fstec is fstec product
```

## GUI migration

FSTEC `@cxado/gui` strangler migration runs on branch `fstec/gui-detach-wip` in the fstec repo. Consumer path from cxado: `file:../../../shared/gui`. See [fstec GUI migration status](https://github.com/butbeautifulv/fstec/blob/fstec/gui-detach-wip/docs/architecture/gui-migration-status.md).

## Related domains

| Domain | Repo | Role |
|--------|------|------|
| **Awareness** | [hexenhammer](https://github.com/butbeautifulv/hexenhammer) | Phishing simulation |
| **Knowledge** | [veil](https://github.com/butbeautifulv/veil) | TI graph |
| **Pentest** | [veneno](https://github.com/butbeautifulv/veneno) | Execution |
