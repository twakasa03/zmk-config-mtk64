# zmk-config-mtk64 — MTK64EBT の ZMK ファームウェア設定

`mentako-ya/zmk-config-mtk64` の fork（`upstream`）。`origin` = `twakasa03/zmk-config-mtk64`。
ブランチ `right_left`。**push が GitHub Actions のビルドトリガー**で、`build.yaml` がファームウェアを
GitHub Releases へ公開し `mtk64ebt` リポへも自動 push する（2026-06-27 設定）。

## 現在のステータス（2026-07-25 更新）

**状態: 凍結**
**再開条件: Phase 2 の身体適応が終わり Phase 4（combo / tap-dance / mod-morph）に入るとき**

2026-07-03 に **Phase 2-A（Home Row Mods: GACS 配列 / バイラテラル / timeless）＋句読点 combo** を
定義してビルドまで通した。ファームウェア側でいま打つ手は無い。

**残っている作業は「体に定着させること」でコミットを生まない。** そちらの進行管理は personal-dx が正本:
- 進捗の正本: [personal-dx/runbooks/phased-rollout.md](../personal-dx/runbooks/phased-rollout.md)（`/phase-status` で現在地）
- 決定の経緯: [personal-dx/docs/99-decisions-log.md](../personal-dx/docs/99-decisions-log.md)

したがってこのリポジトリの停滞日数が伸びるのは正常。**停滞を理由に触らない。**

## 触るときの注意

- キーマップの実体は `config/mtk64.keymap`。日本語キーコードは `config/keycode_japanese.h`
- 軽い変更は ZMK Studio（右手側をUSB接続 → https://zmk.studio/）でも可。ただし **HRM は Studio では定義できない**ので
  ここのファイルを編集して push する
- 変更前に現状キーマップを `personal-dx/exports/` に退避する（personal-dx の作業ルール）
- `upstream` からの取り込みで `config/` が衝突しうる。fork 側の変更は Phase 2-A のコミットに集約されている

## 関連

- 設計プラン全体: personal-dx スコープ1（キーボードファームウェア）
- 身体事情（右手首腱鞘炎・薬指違和感）: [personal-dx/docs/01-body-pain-history.md](../personal-dx/docs/01-body-pain-history.md)
- ベンダーの元 README: [README.md](README.md)
