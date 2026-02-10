# AGENTS

## Repository overview
- This repo stores TamperMonkey userscripts that streamline Azure DevOps work item hierarchy reporting.
- Scripts are maintained as plain-text userscript files (`.txt`) intended to be pasted into TamperMonkey.

## Key files
- `ado-printer.txt`: **Contextual** variant. Injects a compact toolbar into each Azure DevOps work-item form container (`.work-item-form-page`), auto-discovers the current work item ID from DOM links, and supports item/tree output in text/Markdown/HTML to console or clipboard.
- `ado-printer-popup-dom.txt`: **Global control-bar** variant. Renders a fixed toolbar at the top of the page with manual ID refresh from URL context, then outputs item/tree data in text/Markdown/HTML to console or clipboard.
- `README.md`: User-facing install and usage documentation for both script variants.

## Conventions
- Keep scripts TamperMonkey-compatible (userscript metadata block and `GM_*` APIs as needed).
- Keep behavior descriptions in `README.md` aligned with actual script behavior.
- Hierarchy traversal currently excludes `Removed` items and stops descending below `User Story`/`Bug` levels; document any future behavior changes.
- There are no automated tests in this repo; validate behavior manually in Azure DevOps + TamperMonkey when script logic changes.

## Maintenance requirements
- After each work request, review this `AGENTS.md` for newly learned repository knowledge and update when useful.
- After each work request, review `README.md` and keep it accurate to current script behavior and naming.
