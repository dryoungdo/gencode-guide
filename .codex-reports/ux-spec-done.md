# UX Spec Done Report

PR: https://github.com/dryoungdo/gencode-guide/pull/6

## What changed

- Added a marked `index.html` section: `13 · UX/UI Spec สำหรับ Pym`.
- Marked the section `DRAFT v0.1 — for owner + Pym review`.
- Specified requirements for:
  - Thai-name to GENCODE search, including confidence/flag/confirm behavior.
  - Cascading code-builder: TYPE → SUBTYPE → CATEGORY → DIFFERENTIATOR → SEQ → VARIANT → optional VERSION.
  - Order-entry flow, validation gates, and code-breakdown view.
  - Fixed GENCODE boundaries vs Pym's screen/flow design freedom.
- Added a sidebar nav link to the new section and renumbered `ขั้นต่อไป` to section 14.

## Source discipline

- Kept this as a requirements spec, not a visual mockup.
- Did not edit the existing `<style>` block.
- Pointed to YD_GENCODE sources instead of copying token catalogs.
- Concrete GENCODE examples used in the new section are sourced from `CRS-CODE.md` v3.9 or mapper tests:
  - `CRS-SUR-INI-NOSE-SEMI-001-DRDO`
  - `CRS-SKN-INI-BTX-ALG-001-100U`
  - `CRS-SKN-INI-FIL-RST-001-4CC`

## Checks

- `git diff --check`
- Style block diffed clean against `origin/main:index.html`.
- Structural checks confirmed `#uxspec`, the sidebar link, the draft label, source link, and section renumbering.

Browser note: the Browser plugin instructions were read, but the required Node REPL browser-control tool was not exposed in this session, so browser rendering verification could not be run through the in-app browser.
