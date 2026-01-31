# TamperMonkey Scripts for Azure DevOps

This repository contains TamperMonkey user scripts that streamline Azure DevOps work item workflows.

## Files

- `ado-printer.txt`: TamperMonkey script that adds a toolbar to Azure DevOps to fetch a work item hierarchy (or a single item) and output it in text, Markdown, or HTML via console logging or clipboard copy. It stops traversing at Epics, skips Closed/Removed items, and includes a control bar for selecting scope and output format.
- `ado-printer-popup-dom.txt`: TamperMonkey script variant that injects a toolbar directly into the Azure DevOps work item form. It discovers work item IDs from the page DOM, then fetches hierarchy data and outputs it through console logging or clipboard copy.

## Usage

1. Install the TamperMonkey browser extension.
2. Create a new userscript in TamperMonkey and paste the contents of the desired `.txt` file.
3. Navigate to Azure DevOps; the toolbar will appear on matching pages where you can generate and copy the hierarchy or single-item details.

## Maintenance

- `AGENTS.md` contains agent-focused context and workflow expectations for maintaining these scripts.
- Update `README.md` and `AGENTS.md` whenever project details change so future edits stay efficient and accurate.
