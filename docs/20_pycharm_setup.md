# PyCharm setup

## Purpose
This document describes the standard PyCharm configuration
used for Python development in this repository.

The goal is to ensure a consistent and reproducible setup
across Windows and macOS environments.

---

## Interpreter configuration

### Policy
- One virtual environment (`.venv`) per project
- Do not use global Python interpreter
- Interpreter is configured at project level

### Steps
1. Open **Settings / Preferences**
2. Go to **Python Interpreter**
3. Select the project interpreter
4. Choose the `.venv` directory created in `docs/10_python_venv.md`

---

## Project structure recognition
Ensure PyCharm correctly recognizes the project structure:

- Project root is the repository root
- `.venv` is excluded from indexing
- `configs/` and `docs/` are included as project directories

---

## Linting (pylint)

### Policy
- Linting is enabled via **pylint**
- Configuration is project-specific
- Global IDE rules are avoided

### Setup
1. Install pylint in the active venv
2. Enable pylint in PyCharm settings
3. Point PyCharm to the project interpreter
4. Use `configs/pylint/pylintrc` as the configuration file

---

## Terminal configuration
- Use PyCharm built-in terminal
- Ensure `.venv` is activated before running commands
- Avoid mixing system shell and IDE shell unintentionally

---

## Code style
- Follow default PyCharm Python style
- Prefer readability over aggressive formatting
- Avoid premature optimization of formatting rules

---

## Common pitfalls

### PyCharm uses wrong Python
- Re-check interpreter selection
- Verify `.venv` path
- Restart PyCharm if necessary

### pylint not detected
- Ensure venv is activated
- Confirm pylint is installed in the project venv
- Check that PyCharm points to the correct interpreter

---

## Notes
- IDE settings may evolve as the project grows
- Changes should be documented when affecting reproducibility
