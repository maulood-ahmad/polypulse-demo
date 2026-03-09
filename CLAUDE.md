# PolyPulse

Python analytics pipeline for Polymarket prediction data.

## Stack
Python 3.12, Pydantic v2, DuckDB, pandas, matplotlib, click

## External Tool
Polymarket CLI — `polymarket -o json <command>` for all data.
All commands are read-only, no wallet needed.

## Session Workflow
Every Claude Code session is isolated — no session knows what another
session is doing. Files are the coordination layer.

When starting a new session:
1. Read TODO.md for current task list and statuses
2. Read PROGRESS.md (if it exists) for context on what has been done
3. Pick up an unassigned task and mark it In progress in TODO.md
4. Do not edit files that belong to another task (check TODO.md for ownership)

When finishing work:
1. Mark your task Done in TODO.md
2. Update PROGRESS.md with: what was accomplished, files created/modified,
   known issues, and what the next session should pick up
3. Commit with conventional commits (feat:, fix:, chore:)

## Conventions
- Pydantic v2: model_validate(), Field(), ConfigDict
- subprocess.run with capture_output=True, text=True, timeout=30
- loguru for logging (no print statements)
- All functions have type hints and docstrings
- Conventional commits (feat:, fix:, chore:)
