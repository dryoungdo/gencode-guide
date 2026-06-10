# AGENTS.md - the Codex worker contract for gencode-guide

Codex reads **this file**, not `CLAUDE.md`. This is the persistent contract for
the GENCODE guide site so guide-edit tasks inherit the rules even when an
inline brief is incomplete.

This repo **displays** GENCODE for the team. It does **not author** the codes.
The source of truth is
[`dryoungdo-wellness-clinic/YD_GENCODE`](https://github.com/dryoungdo-wellness-clinic/YD_GENCODE):
`CRS-CODE.md` v3.9 plus the tested `mapper/` (307/307 gold).

## Before you touch anything

1. **`git fetch` + read `origin/main` first.** Make no claim about repo state -
   "X exists", "Y is merged", "the guide already says Z" - from a stale clone.
2. Read the relevant guide surface directly (`index.html` today, future `docs/`
   if added). Do not work from memory or chat summaries.
3. If a guide change mentions a GENCODE, verify it against YD_GENCODE before it
   appears in user-facing copy.

## Display-only code discipline

- Every GENCODE shown in this guide must trace to YD_GENCODE. Prefer the tested
  `mapper/` over prose when they disagree; otherwise cite the matching spec
  file and section/line.
- Never invent a code. If a code cannot be verified, **flag it** as a gap for
  human ratification instead of displaying a fabricated value.
- The guide once shipped invented codes like `BDEV` / `MKA`; do not repeat that.
- **Point, don't copy.** Link to YD_GENCODE for the authoritative catalog. Do
  not restate the full token list inline, because copied catalogs drift.

## Guide editing rules

- **Preserve the design.** This is a published site. Content edits only.
- Do not touch CSS, fonts, palette, layout, the `<style>` block, or shared
  stylesheet assets. Change copy, tables, code values, and sections only.
- Comparison tables must mark **existing vs newly-added** codes clearly; the
  guide's job is to show the team what changed.
- No mock data, placeholder fixtures, dead code, or unreferenced helpers.
- If a requested change needs visual work, stop and flag that it violates this
  guide contract unless the human explicitly changes the contract.

## Done means checked

- Re-read the edited content and verify every displayed code has a source.
- If you touch HTML, make sure the page still parses and the changed copy is in
  the intended section.
- Keep the diff narrow. Do not reformat the single-page site while editing copy.

## Finishing a task

1. **Stage by explicit path** - use `git add AGENTS.md` or the named files,
   never `git add -A` / `.`.
2. **Branch off `main`** - never commit directly on `main`.
3. Commit with a co-author trailer identifying the worker.
4. Push the branch, open a PR with base `main`, and include `Closes #<issue>`.
5. **Do not merge.** The human ratifies. Report back the PR link and summary.

---
*The Codex contract for gencode-guide - display-only GENCODE guide discipline.*
