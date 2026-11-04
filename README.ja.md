# Paperwork Fieldnotes

[English](README.md) · [日本語サイト](https://blog.optmodel.com/ja/)

英日二言語の静的blogです。再現できる調査パック、移動できる引き継ぎ、出典ページと財務期間のラベル分けという三つの独自実践を掲載します。

## 導入と実行

Node 24以降とnpmが必要です。依存関係の取得時には通信します。

```sh
git clone https://github.com/kolmo2026/paperwork-fieldnotes.git
cd paperwork-fieldnotes
npm ci
npm run build
npm run serve -- --port 4173
```

サーバー起動後にhttp://127.0.0.1:4173を開きます。停止はCtrl+Cです。

## 再現できる例

**入力：** 編集元はsite/content.mjsとsite/style.cssです。

**出力：** 英日ホーム、About、独自記事3本の計10 HTMLページ、およびsitemap.xml、robots.txt、CNAME。

サンプル：Articles contain synthetic folder structures, page recipes and share scenarios.。同梱文書と数値はすべて合成例です。

## テストとビルド

```sh
npm test
npm run build
```

サイトの編集元は`site/`、生成手順は`scripts/`です。ツール実装は`src/`、核となるテストは`test/`にあります（blogには計算エンジンはありません）。独立した静的サイトを`docs/`に生成し、英日対応ページ、canonical/hreflang、sitemap、robots、CNAME、.nojekyllを含めます。公開用ホストはhttps://blog.optmodel.comです。隣のリポジトリに依存せず単独でビルドできます。


## 制約

合成例を使う学習用手順です。アップロード先、バックエンド、解析、ログインはありません。製品サイトの教程はコピーせずリンクします。

## プライバシーとツール

アカウント、アクセス解析、バックエンド、文書のアップロード先はありません。計算とファイル処理はローカルです。ただし公開サイト資源の取得には通信します。ブラウザー依存ライブラリーは同梱し、実行時CDNは使いません。JSONは平文なので、共有前にファイル名や条件を確認してください。

[Eqvero](https://eqvero.com/)、[KolmoPDF](https://www.kolmopdf.com/)、[KomoPDF](https://komopdf.com/)はツールです。


## ライセンス

MIT。[LICENSE](LICENSE)を参照してください。依存ライブラリーにはそれぞれのライセンスが適用されます。依存導入後のビルドでは、その本文をTHIRD-PARTY-NOTICES.txtに集めます。
