# PPTX Prompter 1.1 — Stage L4-2: 日英対応GitHub Pages

## 収録ファイルと公開URL

GitHub Pagesの公開リポジトリ **`pptx-prompter` のルート**に、以下のファイル構成で配置してください。ZIPそのものをアップロードするのではなく、展開後のファイルを配置します。

```text
index.html              ← 既存日本語トップ（URL維持）
privacy.html            ← 既存日本語プライバシーポリシー（URL維持）
support.html            ← 既存日本語サポート（URL維持）
en/
    index.html          ← 英語トップ
    privacy.html        ← 英語プライバシーポリシー
    support.html        ← 英語サポート
README.md
```

日本語ページ：
- https://naotonaoton999.github.io/pptx-prompter/
- https://naotonaoton999.github.io/pptx-prompter/privacy.html
- https://naotonaoton999.github.io/pptx-prompter/support.html

英語ページ：
- https://naotonaoton999.github.io/pptx-prompter/en/
- https://naotonaoton999.github.io/pptx-prompter/en/privacy.html
- https://naotonaoton999.github.io/pptx-prompter/en/support.html

トップ・プライバシー・サポートの**各ページ右上に日本語／Englishリンク**を追加しました。同じ種類のページへ直接切り替わります。ブラウザの言語による自動転送は行いません。既存の日本語URLはそのまま利用できます。

## 日本語版の変更箇所

- 各ページ右上に言語リンク、headにhreflangリンクを追加。
- `privacy.html` の冒頭を、**表示設定はユーザーのMac内に保存される**という実装に即した記述に修正。従来の「ユーザーデータを保存しません」は、フォントサイズ等をUserDefaultsに保存する実装と紛らわしいためです。プレゼンテーションを外部送信しないという約束は変更していません。
- それ以外の日本語説明・既存リンク・メールアドレス・Apple Events説明は維持。

## GitHubへの反映手順

1. 既存のGitHubリポジトリを開き、現在のサイトを必要に応じてバックアップまたはcommitで保全します。
2. ルートの `index.html`、`privacy.html`、`support.html` を同名ファイルで置き換え、`en/` フォルダの3ファイルを追加します。
3. GitHub Pages が main ブランチの `/ (root)` を公開する設定ならそのままで構いません。GitHub Pagesの公開元が `docs/` 等の場合には、**その公開元**へ配置してください。
4. GitHubで commit 後、上記6つのURLをブラウザで表示し、日英切替・ページ内リンク・サポート用メールアドレスを確認してください。反映まで少し待つ場合があります。
5. App Store Connectの日本語メタデータの現行URLは変えません。英語ローカライズ欄では可能なら英語トップ・英語サポート・英語プライバシーのURLを使い、該当欄が言語別設定できない場合は既存URLでも**ページ右上から英語へ移動可能**です。

## 今回変更していないもの

- MacアプリのSwiftソース・Xcode設定・Build番号
- App Store Connectの公開国、価格、メタデータ
- JavaScript、外部Webサービス、アクセス解析（追加していません）

## 公開前チェック

- 日本語版・英語版の計6ページすべて表示されること
- Privacy / Support / Top の相互リンクが正しいこと
- 日本語版の既存URLが404にならないこと
- 英文・プライバシーポリシーの内容が実際の実装と一致していること
- 英語版サイトの内容に納得できたらVersion 1.1のApp Store審査準備へ進むこと
