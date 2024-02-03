# marp-starter-kit-ja

[Marp](https://marp.app/)は[Markdown](https://www.markdown.jp/syntax/)という記法でプレゼンテーションスライドを作成できるツールです。

## 実行環境

- Windows 10/11
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

- VSCodeでダウンロードしたフォルダを開く
- `Ctrl+,`で設定画面を表示
- 「設定の検索」に`marp`と入力
    -  `Markdown › Marp: Enable HTML`にチェックを入れる
    - `Markdown › Marp: Themes`の「項目の追加」を選択
        - `.\themes\mydefault.css`と入力 → 「OK」

## スライドの出力

- `slides.md`を開く
- パネル上部右端にあるMarpアイコンをクリック
- `Export Slide Deck...`を選択 → 保存先の選択
- `slides.pdf`の生成を確認

## 出力形式の変更

- `Ctrl+,`で設定画面を表示
- 「設定の検索」に`marp`と入力
    - `Markdown › Marp: Export Type`から「PDF」や「pptx」を選択

## ページ番号の削除（スライド単体）
- タイトルページ参照
```
---
<!-- _paginate: false -->
```

## ２コラムレイアウト
- 以下は、左コラムを左寄せ、右コラムを中央寄せに設定している
  - 画像を配置したい場合や箇条書きを2列にしたい場合など
  - 両方とも左寄せにしたい場合は、`style="text-align:center"`を削除
```
<div class="row">
<div class="column">

左コラムコンテンツ

</div>
<div class="column" style="text-align:center">

右コラムコンテンツ

</div>
</div>
```

## 画像の挿入

- 画像ファイルは`images`フォルダに保存しておく
- 画像のサイズは`[w:32, h32]`等で設定する

```
![w:32](./images/画像ファイル名)
```


## PDFエクスポートの不具合

- もしエクスポートしたPDFがVSCode内のプレビューと異なっていたら、Markdownファイルのエンコーディングを確認しましょう
    - "UTF-8 with BOM" を "UTF-8" で保存し直すと不具合が解消されます

## その他の情報

- https://marpit.marp.app/markdown
- https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode
