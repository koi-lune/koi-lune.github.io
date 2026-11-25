# Koi Lune URL移行・動作確認

確認日：2026年11月26日（日本時間）

- 新公開URL：https://koi-lune.github.io/
- 公開用リポジトリ：https://github.com/koi-lune/koi-lune.github.io
- 自動テスト・デプロイ：https://github.com/koi-lune/koi-lune.github.io/actions/runs/45721331766
- 旧公開URL：https://pyokoyu.github.io/koi-lune/ （維持）

## 結果

GitHub ActionsのビルドとPagesへのデプロイが成功。Nodeの14件、Chromiumの17件、WebKitの17件、合計48件の自動テストがすべて成功しました。ブラウザテストのエラーは0件です。公開用ディレクトリをドメイン直下 `/` で配信して検証しました。

スマートフォン相当の幅320・375・390・430・768pxと、デスクトップ1440pxで表示を確認しました。タッチ操作を含むブラウザエミュレーションでの確認で、実機による確認ではありません。

新公開URLでも、タロット、相性占い、恋みくじ、8問の心理テスト、全6章の恋物語をそれぞれ結果まで操作しました。PNG画像保存、効果音の切り替え、Xシェアリンクに新URLが含まれることを確認しました。SNSへの投稿は行っていません。

自動テストでは画像読み込み、保存・再読込、ストーリー再開、コピー、図鑑、入力検証、保存領域の破損・拒否時の動作、キーボード、動きを減らす設定も確認しています。

## 変更箇所

無料Organization `koi-lune` を作成し、`pyokoyu/koi-lune` の最新版を公開リポジトリ `koi-lune/koi-lune.github.io` にフォークしました。新リポジトリのGitHub PagesとActionsを有効にしました。

移行に伴うファイル変更は、ブラウザテストの配信パスを `/koi-lune/` から `/` に対応させたこと、READMEの公開URL・リポジトリ表記、および本レポートです。

コピー元のコミット `3377ed18173b0fe0ca3f78132596c254746970f8` と、新リポジトリの次の9ファイルのGit blob SHAが一致しています。ゲーム本体・デザイン・画像は変更していません。

- index.html
- app.js
- engine.js
- data.js
- style.css
- assets/hero.webp
- assets/cat.webp
- assets/tarot-atlas.webp
- assets/icon.svg

旧リポジトリと旧URLは維持し、旧URLが開くことも確認しました。GitHubユーザー名、釣りゲーム、note自動生成システムは変更していません。有料サービス・有料API・有料ドメインは使用していません。

## 保存データについて

保存データはブラウザのドメインごとに管理されるため、旧URLの履歴や図鑑は新URLへ自動移行しません。旧データは同じブラウザの旧URLに残り、新URLでは別の保存データとして始まります。
