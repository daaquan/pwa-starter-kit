# Offline ToDo PWA

このサンプルは、ブラウザのホーム画面に追加できるシンプルな ToDo リストの PWA です。
依存ライブラリを使用せず、HTML/JavaScript/CSS だけで構成されています。

## 使い方

1. このリポジトリをクローンします。
   ```bash
   git clone <this repo url>
   cd pwa-starter-kit
   ```
2. ローカルサーバーを起動します（Python を例にしています）。
   ```bash
   python3 -m http.server 8000
   ```
3. ブラウザで `http://localhost:8000/index.html` を開きます。
4. "ホーム画面に追加" することでオフラインでも利用できます。

## ファイル構成

- `index.html` - ToDo リスト本体
- `service-worker.js` - オフラインキャッシュ用のサービスワーカー
- `manifest.json` - PWA 設定 (アイコンは Base64 データ URI として埋め込み)

## デスクトップアプリとして実行 (Electron)

Electron を利用してデスクトップアプリとして起動できます。

```bash
npm install
npm start
```

## モバイルアプリとして実行 (Capacitor)

以下のコマンドで各プラットフォーム用のプロジェクトを生成できます。

```bash
npm run copy           # Web アセットをネイティブプロジェクトへコピー
npm run build:ios      # iOS プロジェクト生成
npm run build:android  # Android プロジェクト生成
```

生成された `ios/` や `android/` ディレクトリでビルドや実機確認を行ってください。

## ライセンス
MIT
