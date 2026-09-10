# シナリオ・テンプレート

新しいシナリオは、このディレクトリの中身をシナリオ用の場所（別ブランチ等）へコピーして始める。
規約の根拠は `method/`（`00-constitution` / `01-review-protocol` / `02-document-layout` / `04-character-protocol`）。

## 記入順序（憲法第3条：骨→肉）

**骨（順序固定・必須）**
1. `spec/00-anchor` … 核を確定（**型**＝シーン型／人物型、抽象面＋具体面、正副、Locked/Open）
2. `spec/10-opposition` … 対立軸（壁）。味方より先に
3. `spec/20-origin` … 主人公の初期状態（アンカーから逆算）
4. `spec/30-spine` … 因果の背骨（ビート列）

**肉（自由順）**
5. `spec/40-cast/` … 配役。**1キャラ＝1フォルダ**（`_character/` をコピー。`04-character-protocol` に従う）
6. `spec/50-world/` … 世界・設定（`_topic.template.md` をコピー、必要駆動）

> 人物型アンカーを選んだ場合、正アンカー人物も `40-cast/` にフォルダを持ち、核の実体はそこに置く。
> `00-anchor` はそれを語幹参照で指すだけにする（`04-character-protocol` 第4節）。

そのうえで生成単位ごとに `plans/` → `output/` を回す。

## ステータス（＝信頼度）の扱い

- 各ファイルは `.draft`（暫定）で作り、審査（`01-review-protocol`）を通過し承認されたら `.locked` にリネームする。
- 参照は接尾辞を含まない**語幹**（例 `30-ten`、`spec/00-anchor`）で書く。
- `decisions/`（決定ログ）と `ideas/`（採否未定のアイデア置き場）はステータスを持たない追記型。信頼度パイプラインの外。
- `ideas/` は**本編に勝手に混ぜない**バッファ。採用したら `spec/plans` の `.draft` か `decisions/` へ移送し、元エントリに移送先を追記する（`02-document-layout` 第7節）。

## `_*.template.md` フォームの使い方

`_` で始まるファイル／フォルダはコピー元のフォーム。コピーして `NN-<名前>.draft.md` にリネームし、
先頭のコピー指示コメント行を削除して使う。

- `_topic.template.md`（世界）… 単一ファイルをコピー。
- `_character/`（配役）… **フォルダごと** `NN-<character>/` にコピーし、中の各ファイル（`00-core` / `10-voice` / `20-relations` / `30-arc`）を `.draft.md` にリネームする。ステータスはファイル単位で付く（核だけ先に `.locked`、が可能）。
