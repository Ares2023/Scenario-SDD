# シナリオ・テンプレート

新しいシナリオは、このディレクトリの中身をシナリオ用の場所（別ブランチ等）へコピーして始める。
規約の根拠は `method/`（`00-constitution` / `01-review-protocol` / `02-document-layout`）。

## 記入順序（憲法第3条：骨→肉）

**骨（順序固定・必須）**
1. `spec/00-anchor` … 核を確定（Scene＋Message、正副、Locked/Open）
2. `spec/10-opposition` … 対立軸（壁）。味方より先に
3. `spec/20-origin` … 主人公の初期状態（アンカーから逆算）
4. `spec/30-spine` … 因果の背骨（ビート列）

**肉（自由順）**
5. `spec/40-cast/` … 配役（`_character.template.md` をコピー）
6. `spec/50-world/` … 世界・設定（`_topic.template.md` をコピー、必要駆動）

そのうえで生成単位ごとに `plans/` → `output/` を回す。

## ステータス（＝信頼度）の扱い

- 各ファイルは `.draft`（暫定）で作り、審査（`01-review-protocol`）を通過し承認されたら `.locked` にリネームする。
- 参照は接尾辞を含まない**語幹**（例 `30-ten`、`spec/00-anchor`）で書く。
- `decisions/` はステータスを持たない追記型の記録。

## `_*.template.md` フォームの使い方

`_` で始まるファイルはコピー元のフォーム。コピーして `NN-<名前>.draft.md` にリネームし、
先頭のコピー指示コメント行を削除して使う。
