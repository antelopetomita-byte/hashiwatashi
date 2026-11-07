# Claude Code サブエージェント（ハシワタシ）

| 名前 | モデル | 役割 |
|---|---|---|
| implementer | sonnet | index.html の実装・修正（編集可） |
| ui-mobile-checker | haiku | スマホ表示・操作・アクセシビリティの点検（読み取り専用） |
| reviewer | sonnet | 差分/全体のレビュー・秘密情報チェック（読み取り専用） |

## 並列依頼の例
> ui-mobile-checker と reviewer を並列で動かして、index.html を点検して。結果を重要度順にまとめて。

実装→確認の流れ:
> implementer で「ベスト更新時に演出を足す」を実装し、終わったら reviewer と ui-mobile-checker を並列で実行して。
