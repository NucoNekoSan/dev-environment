# Linting with pylint

## Purpose
This document describes how pylint is used in this repository
to maintain code quality and readability.

The goal is not to enforce strict rules blindly,
but to provide consistent guidance for maintainable code.

---

## Why pylint
- Detect potential bugs early
- Improve code readability
- Encourage consistent coding style
- Support long-term maintainability

---

## Policy
- Linting is applied **per project**
- Global pylint configuration is avoided
- Rules may be adjusted based on project context
- Warnings are treated as guidance, not absolute errors

---

## Installation
pylint is installed as a development dependency inside the project virtual environment.

```bash
pip install pylint
```
It is recommended to manage pylint via a development requirements file.

## Configuration

### Configuration file
- Location: `configs/pylint/pylintrc`
- Scope: Project-specific only

### Why per-project configuration
- Different projects have different complexity
- Avoid unnecessary warnings
- Easier maintenance over time

---

## Running pylint

### From command line

```basn
pylint your_module_or_package
```

### From PyCharm
- Ensure the project interpreter points to `.venv`
- Enable pylint in PyCharm settings
- Use the project configuration file

---

### Handling warnings
- Review warnings carefully
- Suppress warnings only when justified
- Document any significant rule changes

---

## Common issues

### pylint not found
- Ensure virtual environment is activated
- Verify pylint is installed in .venv
- Confirm PyCharm uses the correct interpreter

### Too many warnings
- Start with default rules
- Gradually refine configuration
- Focus on readability over score

---

## Notes
- Linting rules may evolve with project maturity
- Changes should be documented to maintain reproducibility

---

Changes should be documented to maintain reproducibility
