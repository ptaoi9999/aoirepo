# Aoi's Repo - LiveContainer & AltStore Repository

LiveContainer、SideStore、およびAltStoreに対応した、GitHub Pagesでホストできる自作アプリ用リポジトリです。

## 特徴

- **ダイナミック・ロード**: ウェブサイト（`index.html`）は `apps.json` から動的にアプリ情報を読み込みます。`apps.json` を更新するだけでサイト側も自動で連動します。
- **マルチ対応**: AltStoreおよびSideStoreに直接リポジトリを追加するためのワンタップボタン付き。
- **美しいデザイン**: Outfitフォント、半透明のグラスモーフィズムデザイン、グラデーションカラー、マイクロインタラクションを採用したプレミアムなUI。
- **LiveContainer向けの解説**: LcInstallerを使用したLiveContainerへの直接インストールの手順を説明。

## リポジトリの内容

- [index.html](file:///home/aoi/aoirepo/index.html) - リポジトリのWebランディングページ
- [apps.json](file:///home/aoi/aoirepo/apps.json) - アプリのメタデータを管理するJSONファイル（AltStore Source形式）

---

## クイックスタートガイド：GitHub Pagesへの公開手順

このワークスペースのファイルを自身のGitHubリポジトリにプッシュして、GitHub Pagesを有効化することで即座にオンラインで利用可能になります。

### 1. ローカルGitリポジトリの初期化とコミット

```bash
git init
git add .
git commit -m "Initial commit: Set up Aoi's Repo and landing page"
```

### 2. GitHubで新規リポジトリの作成

1. GitHubにログインし、[New Repository](https://github.com/new) を開きます。
2. リポジトリ名を `aoirepo` （またはお好みの名前）にします。
3. リポジトリを「Public（公開）」に設定します。
4. リポジトリを作成します。

### 3. リモートリポジトリの設定とプッシュ

作成したGitHubリポジトリのURLに合わせて、以下を実行します（ユーザー名をご自身のものに置き換えてください）：

```bash
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/aoirepo.git
git branch -M main
git push -u origin main
```

### 4. GitHub Pagesの有効化

1. GitHub上のリポジトリのページを開き、**Settings**（設定）タブをクリックします。
2. 左メニューの **Pages** を選択します。
3. 「Build and deployment」セクションの **Source** を **Deploy from a branch** にします。
4. **Branch** で `main`（または `/ (root)`）を選択し、**Save** をクリックします。
5. 数分待つと、`https://YOUR_GITHUB_USERNAME.github.io/aoirepo/` にてリポジトリページが公開されます！

---

## アプリの追加方法

`apps.json` の `apps` 配列に新しいオブジェクトを追加することで、アプリを追加・更新できます。

### テンプレート例

```json
{
  "name": "アプリ名",
  "bundleIdentifier": "com.developer.appname",
  "developerName": "開発者名",
  "subtitle": "短いサブタイトル",
  "localizedDescription": "アプリの詳細な説明文。",
  "iconURL": "https://example.com/icon.png",
  "tintColor": "#hexcolor",
  "versions": [
    {
      "version": "1.0.0",
      "date": "2026-07-23",
      "localizedDescription": "最初のリリース",
      "downloadURL": "https://example.com/app.ipa",
      "size": 12345678
    }
  ]
}
```
