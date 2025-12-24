# Python virtual environment (venv)

## Purpose
This document describes how to create and use a Python virtual environment
to ensure reproducible development across Windows and macOS.

## Why venv per project
- Avoid dependency conflicts
- Ensure reproducibility
- Easy reset when environment breaks

---

## Windows (PowerShell)

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r configs/python/requirements-dev.txt
```

## If script execution is blocked:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

## macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r configs/python/requirements-dev.txt
```

## Reset environment
If the environment is broken:
- Delete `.venv`
- Recreate venv following the steps above

## Notes
- Do not commit .venv
- Always activate venv before running tools
- Verified on Windows 11 and macOS

---
### ⑤ Commit
- Commit message：  
  `Add Python venv setup documentation`
- Direct commit to main branch：**OK**
- Commit changes
---
