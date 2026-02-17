<!-- Auto-generated guidance for AI coding agents — tailored to this repository. -->
# Repository-specific Copilot Instructions

Purpose
- Provide concise, actionable guidance for AI coding agents working in this repo.

Quick summary
- This repository currently contains a single Jupyter notebook: Projeto_Python_Data_Science.ipynb
- Primary workflow: exploratory data analysis inside the notebook. There is no package layout, tests, or CI detected.

What to do first (high value, low risk)
- Open and inspect `Projeto_Python_Data_Science.ipynb` for cell order, data sources, and key analysis steps.
- Avoid changing notebook cell outputs in-place when making code edits — prefer creating a new code cell or extracting code to a `.py` file instead.

Editing conventions for agents
- If adding reusable code, create a new module directory (for example `src/` or `notebook_helpers/`) and put functions in `.py` files; update the notebook to import those modules.
- Keep notebook commits output-free: clear cell outputs before committing large diffs to reduce noise and merge conflicts.
- Prefer small, incremental PRs: (1) extract code to `.py`, (2) add minimal tests or example usage in a new notebook cell, (3) update README.

Project-specific notes
- File to inspect: `Projeto_Python_Data_Science.ipynb` (root). Use it to identify data-loading paths, plotting code, and long-running cells.
- No tests or build scripts were discovered; do not assume a test framework exists. If you add tests, include a `requirements.txt` or `pyproject.toml` and a short CI step.

Agent behavior guidance
- Preserve the notebook's narrative: keep markdown explanations intact while refactoring code.
- When refactoring, run the notebook locally (or via headless execution) to confirm outputs still render, and report any long-running cells.
- Avoid making broad project-structure changes without a user instruction (e.g., converting to a full package) — present a short proposal first.

Examples (how to make safe edits)
- Extract helper functions: create `notebook_helpers/io.py` and move data-load functions there; in the notebook replace code cells with `from notebook_helpers.io import load_data()`.
- Add documentation: create `README.md` with brief notes on how to run the notebook and any environment recommendations.

When to ask the user
- Before introducing project-wide structure (packages, CI), or adding large dependencies.
- Before deleting or significantly restructuring the only notebook in the repo.

Where to look next
- If the repo grows, look for `requirements.txt`, `pyproject.toml`, `environment.yml`, or any `src/` folder for packaging conventions.

Feedback
- If anything here is incorrect or you want a different agent behavior (e.g., auto-convert notebooks to scripts), tell me and I will update this file.
