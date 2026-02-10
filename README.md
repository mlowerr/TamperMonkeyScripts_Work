# TamperMonkey Scripts for Azure DevOps

This repository contains TamperMonkey user scripts for printing Azure DevOps work item context and hierarchy data.

## Scripts

- `ado-printer.txt` (**Contextual toolbar**)
  - Injects a toolbar directly into each work item form container (`.work-item-form-page`).
  - Detects the current work item ID from work-item links in that container.
  - Supports:
    - Scope: single item or tree
    - Tree mode: direct path + descendants, or full tree from Initiative root
    - Output format: plain text, Markdown, HTML
    - Destination: clipboard copy or console log
- `ado-printer-popup-dom.txt` (**Global top control bar**)
  - Adds a fixed toolbar at the top of Azure DevOps pages.
  - Uses URL-based work item ID detection with manual refresh.
  - Supports the same scope, mode, format, and output options as above.

## Current hierarchy behavior

Both scripts currently:
- Exclude work items in `Removed` state from output.
- Stop downward traversal at `User Story` and `Bug` levels.
- Can include additional detail fields (status, assigned-to) in output formatting.

## Usage

1. Install the TamperMonkey browser extension.
2. Create a new userscript and paste one of the script files from this repo.
3. Open Azure DevOps (`dev.azure.com` or `*.visualstudio.com`) and use the injected toolbar to generate output.

## Maintenance

- `AGENTS.md` stores maintainer/agent workflow notes for repository updates.
- Keep this README aligned with script behavior whenever scripts change.
