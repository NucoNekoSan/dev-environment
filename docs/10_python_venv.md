# Python 仮想環境（venv）

## 目的
このドキュメントは、Windows / macOS 両環境において  
**再現性のある Python 開発環境**を構築・運用するための手順をまとめたものです。

---

## プロジェクトごとに venv を使う理由
- 依存関係の衝突を防ぐため
- 環境の再現性を確保するため
- 問題発生時に簡単にリセットできるため

---

## Windows（PowerShell）

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r configs/python/requirements-dev.txt
```

## スクリプトの実行がブロックされる場合

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

---

## macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r configs/python/requirements-dev.txt
```

## 環境のリセット
環境に問題が発生した場合は、以下の手順で再作成します。
- `.venv` ディレクトリを削除
- 上記手順に従って venv を再作成

## 注意点
- `.venv` は Git にコミットしない
- ツールを実行する前に、必ず venv を有効化する
- Windows 11 / macOS 環境で動作確認済み

---

### Commit
- Commit message：  
  `Add Python venv setup documentation`
- main ブランチへ直接コミット：OK
- Commit changes
---
