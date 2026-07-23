# LinkRelay Repository - LiveContainer & AltStore Source

`LinkRelay-latest.ipa` を配信するための専用リポジトリソースです。GitHub Pagesを有効化してデバイス（LiveContainer、AltStore、SideStoreなど）に簡単に追加・ダウンロードできます。

## 含まれるファイル

- **[index.html](file:///home/aoi/aoirepo/index.html)**: 
  - LinkRelay専用の美しくレスポンシブなランディングページ。
  - サイト上で「Add to AltStore」「Add to SideStore」ボタンで即座に追加可能。
  - アプリダウンロード用IPAリンクは、公開時のドメインに合わせて自動的に解決されます。
- **[apps.json](file:///home/aoi/aoirepo/apps.json)**:
  - AltStore互換のアプリソース定義ファイル。
- **[LinkRelay-latest.ipa](file:///home/aoi/aoirepo/LinkRelay-latest.ipa)**:
  - 配布対象のアプリ実体ファイル。

---

## 公開手順

このリポジトリをGitHub Pagesにアップロードするだけで、自分専用のリポジトリサーバーとして機能します。

### 1. アカウント名に合わせて `apps.json` を変更（推奨）
`apps.json` の以下の部分をお使いのGitHubユーザー名に変更しておくと、AltStoreアプリで読み込んだ際にもエラーなくIPAがダウンロードできます：
```json
"downloadURL": "https://YOUR_GITHUB_USERNAME.github.io/aoirepo/LinkRelay-latest.ipa"
```

### 2. Gitでコミット

```bash
git add .
git commit -m "Configure dedicated repository for LinkRelay"
```

### 3. GitHubへプッシュ＆Pages公開
1. GitHubで **Public** リポジトリ（例: `aoirepo`）を作成。
2. ローカルリポジトリからプッシュ：
   ```bash
   git remote add origin https://github.com/YOUR_GITHUB_USERNAME/aoirepo.git
   git push -u origin main
   ```
3. GitHubリポジトリの **Settings** > **Pages** に移動し、`main` ブランチを選択して **Save**。
4. 数分後、`https://YOUR_GITHUB_USERNAME.github.io/aoirepo/` にアクセスできるようになります！
