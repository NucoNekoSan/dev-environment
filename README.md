# dev-environment

## 概要
このリポジトリは、**Windows / macOS 両対応の再現可能な Python 開発環境**を記録したものです。

環境差分やマシン依存を最小限に抑えるため、  
明確で繰り返し実行可能な手順をドキュメントとして整理しています。

---

## 対象環境
- Windows 10 / 11
- macOS
- Python 3.x
- PyCharm

---

## 内容
- Windows / macOS 向け Python 仮想環境（venv）の構築手順
- PyCharm の設定方法
- pylint を用いた lint 設定
- .gitignore の運用方針
- よくあるトラブルと対処方法

---

## 方針
- プロジェクトごとに 1 つの仮想環境（venv）を使用
- ドキュメントを起点とした運用を重視
- 過度に複雑な構成より、**シンプルで保守しやすい設計**を優先

---

## 使い方
1. `docs/00_overview.md` を読む
2. Python 仮想環境を構築（`docs/10_python_venv.md`）
3. PyCharm を設定（`docs/20_pycharm_setup.md`）
4. lint を有効化（`docs/30_linting_pylint.md`）

---

## ステータス
- 継続的にメンテナンス・更新中

