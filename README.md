# Fastladder (Hashigo Reader) - Modern Rewrite

Fastladder (RSS Reader) の Bun + Hono + Svelte によるリライト版です。
高速かつ軽量な動作を目指して再実装されています。

## 技術スタック

- **Runtime**: [Bun](https://bun.sh) (Node.js互換の高速ランタイム)
- **Backend**: [Hono](https://hono.dev) (Web標準に準拠した軽量フレームワーク)
- **Frontend**: [Svelte 5](https://svelte.dev) (コンパイラベースのUIフレームワーク)
- **Build Tool**: [Vite](https://vitejs.dev)
- **Database**: SQLite (`bun:sqlite` を使用)

## 必要要件

- [Bun](https://bun.sh) (v1.0.0以上推奨)

## セットアップ & 起動

リポジトリをクローンした後、以下の手順でセットアップと起動を行ってください。

```bash
# プロジェクトディレクトリへ移動
cd ts

# 依存関係のインストール
bun install

# 開発サーバーの起動
# バックエンド(Hono)とフロントエンド(Vite)が同時に起動します
bun run dev
```

起動後、ブラウザで [http://localhost:5173](http://localhost:5173) にアクセスしてください。

## ディレクトリ構成

```
ts/
├── server/      # Hono バックエンドサーバーのエントリーポイント
├── frontend/    # Svelte フロントエンドアプリケーション
├── src/         # 共通ロジック
│   ├── crawler/ # RSS/Atom クローラー
│   ├── db/      # データベース接続・操作
│   └── routes/  # API ルーティング定義
├── index.ts     # バックエンドのエントリーポイント
└── vite.config.ts # Vite 設定ファイル
```

## ライセンス

MIT
