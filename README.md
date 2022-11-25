# marp-starter-kit-ja

## 実行環境

- Windows 10
- VSCode

## フォルダ構成

```
marp-starter-kit-ja/
    ├ images/
    │   ├ 画像ファイル
    │   └ ・・・    
    ├ themes/
    │   └ mydefault.css（カスタムテーマ）
    ├ README.md（本ファイル）
    └ slides.md（スライド本体）
```

## カスタムテーマの特徴

- 筑波大のロゴ
- `Default`テーマ + `gaia`フォントサイズ
- デフォルト（スライドクラスなし）：左上寄せ
- `lead`：中央中寄せ

## カスタムテーマの設定

- `slides.md`を開く
- `Ctrl+,`で設定画面を表示
- 「設定の検索」に`marp`と入力
    -  `Markdown › Marp: Enable HTML`にチェックを入れる
    - `Markdown › Marp: Themes`の「項目の追加」を選択
    - `themes\mydefault.css`と入力 → 「OK」

## スライドの出力

- `slides.md`を開く
- パネル上部右端にあるMarpアイコンをクリック
- `Export Slide Deck...`を選択 → 保存先の選択
- `slides.pdf`の生成を確認

## 出力形式の変更

- `Ctrl+,`で設定画面を表示
- 「設定の検索」に`marp`と入力
    - `Markdown › Marp: Export Type`から「PDF」や「pptx」を選択

## フッターの削除（スライド単体）

```
---
<!-- _footer: '' -->
```

## ２コラムレイアウト

```
<div class="row">
<div class="column">

左コラムコンテンツ

</div>
<div class="column">

右コラムコンテンツ

</div>
</div>
```

## PDFエクスポートの不具合

- もしエクスポートしたPDFがVSCode内のプレビューと異なっていたら、Markdownファイルのエンコーディングを確認しましょう
    - "UTF-8 with BOM" を "UTF-8" で保存し直すと不具合が解消されます

## その他の情報

- https://marp.app/
- https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode
