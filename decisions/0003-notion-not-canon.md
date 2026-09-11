# Notion は正典ではない／AI の自己承認を禁止する

## 決定
このブランチ（および今後の同種の作業）において：
1. **Notion の既存ページは参考資料であり、このブランチの正典ではない。**
2. **Locked にできるのは、ユーザーがこの会話で明示的に述べたことのみ。**
3. AI が自分で作った提案・逆算（骨2の起点逆算など）も、ユーザーが確認するまでは Open。
   AI が自分の提案を自分で Locked にしてはならない。

## 背景
アンカー・対立軸・騎士の核・decisions を書く過程で、AI が Notion の正典索引の内容
（怪画の異能機構、画家の20年・病、解放の主体など）をユーザーの確認なしに Locked として書き込んでいた。
さらに、骨2（主人公の初期状態の逆算）で AI 自身が作った提案までも、AI 自身が Locked と自己承認していた。
これは憲法第5条（人間の承認をもって初めて Locked になる）への違反であり、ユーザーから直接指摘を受けて修正した。

影響を受けた箇所（downgrade 済み）：
- `spec/00-anchor.draft.md`（解放の主体・審査メモの機構断定・騎士の対位法の断定を Open へ）
- `spec/10-opposition.draft.md`（怪画設定の Locked 化を撤回、案A／案Bの提案に変更）
- `spec/20-origin.draft.md`（起点提案全体を Locked から「AI提案・要確認」へ）
- `spec/40-cast/10-knight/00-core.draft.md`（能動限定の制約を撤回、2構造を Open な候補として併記）
- `decisions/0001-secondary-anchor-knight.md`（無自覚 vs 自覚の断定を撤回）

## 却下した代替案
なし（プロセス上の誤りの是正であり、代替案の比較は発生しない）。

## 影響する仕様（語幹参照）
- `spec/00-anchor`
- `spec/10-opposition`
- `spec/20-origin`
- `spec/40-cast/10-knight#core`
- `decisions/0001-secondary-anchor-knight`
