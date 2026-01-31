# AGENTS

## Repository overview
- This repo stores TamperMonkey userscripts used to streamline Azure DevOps work item workflows.
- Scripts are stored as plain text files (`.txt`) that can be pasted into TamperMonkey.

## Key files
- `ado-printer.txt`: Adds a toolbar to Azure DevOps pages to fetch a work item hierarchy (or a single item) and output it as text/Markdown/HTML via console logging or clipboard copy.
- `ado-printer-popup-dom.txt`: Variant that injects a toolbar directly into the Azure DevOps work item form; discovers work item IDs from the DOM and outputs via console logging or clipboard copy.
- `README.md`: High-level usage instructions for installing and using the scripts.

## Conventions
- Keep scripts as TamperMonkey-compatible userscript text files.
- Maintain clear, user-focused descriptions of behavior in `README.md`.
- There are no automated tests in this repo; validate changes manually in a browser with TamperMonkey when needed.

## Maintenance requirements
- After completing each work request, review and update **this** `AGENTS.md` with any new project knowledge that should help future changes.
- After completing each work request, review and update `README.md` to keep project information current.
