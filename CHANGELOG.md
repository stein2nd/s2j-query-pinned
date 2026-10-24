# S2J Query Pinned - CHANGELOG

## unreleased

## 0.0.1 - 2026-10-24

### Added

* `phpunit.unit.xml.dist` とユニット PHPUnit のスモークテストを追加。CI は WordPress 未起動の `composer test:unit` を実行する。
* `package.json` に `phpunit:wp-env` を追加し、GitHub Actions「PHPUnit」が未定義 script で落ちないようにした。

### Changed

* WordPress [必須要件](https://ja.wordpress.org/about/requirements/)に合わせ、実行環境の PHP 下限を v8.3にそろえた。`composer.json`、`phpcs.xml.dist`、`phpstan.neon.dist`、`.github/workflows/phpunit.yml`、`.github/workflows/dist-zip.yml`、`docs_mod/specs.md`、`README.md` を更新した。
* GitHub Actions「docs-lint」の paths に `composer.json` を追加した。

## 0.0.1 - 2026-10-15

### Added

* GitHub Actions に配布 zip ビルド (`dist-zip.yml`) と PHPUnit (`phpunit.yml`) を追加
* `tools/dist/make-dist-zip.mjs` で本番ビルドから配布 zip を生成

### Changed

* 開発依存 npm を更新 (React v19.3.1、Rollup v4.64.7、`@s2j/docs-linter` v1.0.29、`@typescript-eslint/*` v8.71.2等)
* textlint の許可パターンに `#status-*` アンカー ID を追加

## 0.0.1 - 2026-10-11

### Changed

* 開発依存 npm を更新 (`@wordpress/components` v42、`@wordpress/element` v9、Vite v8.3.4、Rollup v4.64.5、`@typescript-eslint/*` v8.71.1等)
* 開発依存の `braces` v3.0.3 (GHSA-vfj7-8cjw-p6xm) は修正版が未公開のため、深刻度 high の指摘7件 (CVE-2026-93687) は残す。

## 0.0.1 - 2026-10-10

### Changed

* 仕様ドラフトの Archive 組立手順で、「サービスへ渡す」を「サービスに渡す」にした。

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
