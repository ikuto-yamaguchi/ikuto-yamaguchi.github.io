# Life Garden / ikuto-yamaguchi.github.io

このリポジトリはライフゲームをベースにしたブラウザゲーム「Life Garden」の GitHub Pages 公開用ソースです。静的 HTML/CSS/JS で構成されており、ローカルでも簡単に確認できます。

## ローカル確認方法
1. Python がインストールされている環境で以下を実行します。
   ```bash
   python -m http.server 8000
   ```
2. ブラウザで http://localhost:8000 を開き、PC とスマートフォンの画面幅で挙動を確認してください。
3. スマホ表示はデベロッパーツールのデバイスモードまたは実機で確認するとレイアウト崩れを把握しやすいです。

## GitHub Pages / デプロイについて
- この開発環境から **git push は行っていません**。GitHub への反映や Pages での表示確認は、リポジトリ管理者の権限で実施してください。
- `git push` を実行するには、先にリポジトリ URL を指定してリモートを追加してください（例: `git remote add origin <repository-url>` のうえで `git push origin work` など）。本環境ではリモート未設定のため、`git push` を試行すると「No configured push destination」と表示されます。
- GitHub Pages での最新ビルドを確認する際は、push 後に数分程度の反映遅延が生じることがあります。キャッシュが残る場合はシークレットウィンドウでアクセスしてください。
- デプロイ状況に問題がある場合は、GitHub Actions（利用している場合）や Pages のビルドログを確認してください。

### リモート設定の確認と push 手順
1. リモート設定を確認します。
   ```bash
   git remote -v
   ```
   何も表示されない場合はリモート未設定です。
2. リモートを追加します（URL はご自身のリポジトリに置き換えてください）。
   ```bash
   git remote add origin https://github.com/<OWNER>/<REPO>.git
   ```
3. 現在のブランチ（例: `work`）を push します。
   ```bash
   git push -u origin work
   ```
4. push 後、GitHub Pages の反映を待ち、ブラウザのキャッシュをクリアして最新を確認してください。

> なお、リモート未設定の場合でもローカルのコミットは失われません。適切なリモートを設定したうえで push すれば、これまでの変更を GitHub に反映できます。

## 主なページ
- `index.html`: ゲーム本体と概要ページ
- `about.html` / `about-en.html`: ゲームの特徴と更新履歴
- `faq.html` / `faq-en.html`: よくある質問
- `terms.html` / `terms-en.html`: 利用規約
- `privacy.html`: プライバシーポリシー

## ライセンス
本リポジトリのコンテンツに関する権利は著作者に帰属します。利用に関する詳細は `terms.html` を参照してください。
