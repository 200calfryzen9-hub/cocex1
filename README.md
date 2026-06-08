# WagyuMate Refined

黒毛和牛の繁殖・分娩・子牛管理を行うための React/Vite アプリです。

## 主な機能

- 母牛一覧、子牛一覧、個体詳細管理
- 授精、妊娠鑑定、分娩、発情、治療、メモの記録
- 分娩予定、再発情確認、妊娠鑑定、乾乳目安のカレンダー表示
- 分娩後日数、空胎日数、初回授精目安に基づくアラート
- ダッシュボードで妊娠率、種付後、空胎・休養頭数を確認
- Firebase Realtime Database を使った家族共有設定
- PWA 用 manifest とアイコン付き

## GitHub へアップロードする方法

1. このフォルダの中身を GitHub の新しいリポジトリにアップロードします。
2. GitHub の `Settings` → `Pages` を開きます。
3. `Build and deployment` の `Source` を `GitHub Actions` にします。
4. `main` ブランチへアップロードまたは push すると、自動でビルドされます。

## ローカルで動かす場合

ローカル確認には Node.js が必要です。

```bash
npm install
npm run dev
```

本番用にビルドする場合:

```bash
npm run build
```

## Firebase 共有について

アプリ内の設定画面から Firebase 設定 JSON と家族IDを入力すると、複数端末でデータ共有できます。
Firebase を使わない場合でも、ブラウザの localStorage に保存されます。
