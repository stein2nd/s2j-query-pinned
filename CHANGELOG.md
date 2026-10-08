# S2J Query Pinned - CHANGELOG

## unreleased

## 0.0.1 - 2026-10-08

### Changed

* 仕様ドラフトの文言を、ドキュメント lint に合わせた。「とき」は「場合」または「際」、「次」は「下記」にした。

## 0.0.1 - 2026-10-05

### Changed

* 仕様ドラフトで、一覧のピン留め列を初版に含めた。初期値は出さない。サイト全体の `s2j_query_pinned_column` と、タイプごとの `show_column` で出し分ける。添付ファイルの列はメディアライブラリに出す。
* Composer の `s2j/query-pinned-service` は、S2J Slug Generater と同じく Packagist のパッケージ名だけで require する。
* `show_ui` だけで `public` ではない CPT も、設定の表に出す。
* 固定記事の Query Loop は、「ピン留めを先頭にする」の初期値を off にし、そのブロックだけ on にできる。
* アンインストールで消す対象に、オプション `s2j_query_pinned_column` を加えた。

## 0.0.1 - 2026-10-04

### Added

* プラグイン仕様ドラフトを `docs_mod/specs.md` に記載
* npm v12以降向けに `.npmrc` の `allow-git=all` と `package.json` の `allowScripts` を追加

### Changed

* 開発依存の `braces` v3.0.3 (GHSA-vfj7-8cjw-p6xm: 深くネストしたパターンで Node.js プロセスが終了する) は修正版が未公開のため、深刻度 high の指摘7件 (CVE-2026-93687) は残す。
