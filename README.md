# Rainy Muse Preview

Rainy Muse の各Webプロジェクトを、本番を変更せずに検証するためのプレビュー専用リポジトリです。

- URL: `https://ennea5w4.github.io/preview/<project>/`
- 1プロジェクト＝1フォルダ（フォルダ名は本番リポジトリ名と同じにする。パス判定がリポジトリ名に依存するプロジェクトがあるため）
- 各フォルダの `PREVIEW_SOURCE.txt` に元リポジトリ・ブランチ・コミットを記録する

## ルール
- 置くのは検証対象のWeb公開ファイルだけ
- 商品用マスター原本・個人情報・認証情報・バックアップは置かない
- 全HTMLに `<meta name="robots" content="noindex,nofollow,noarchive">` を入れる（プレビュー側だけの変更。本番ブランチには入れない）
- 本番リポジトリの GitHub Pages 設定は変更しない

## 更新手順（例：sleeping-stars-v2）
1. 本番リポジトリで対象コミットを `git archive <commit> index.html en ko js img` で書き出す
2. このリポジトリの `sleeping-stars-v2/` を置き換える
3. 3つのHTMLに noindex メタタグを追加し、`PREVIEW_SOURCE.txt` を更新してコミット
