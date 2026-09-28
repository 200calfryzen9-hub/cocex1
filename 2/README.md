# WagyuMate

和牛農家向けの牛群・繁殖管理アプリです。母牛と子牛の情報、繁殖履歴、分娩予定、子牛の血統・販売情報を管理します。

## 開発環境

- Node.js
- npm

## 起動

```powershell
npm ci
npm run dev
```

本番用ファイルの生成:

```powershell
npm run build
```

## データについて

アプリの基本データはブラウザの`localStorage`に保存します。設定画面でFirebase Realtime Databaseを設定すると、複数端末間で同期できます。GitHubへアップロードする前に、個人情報や本番環境の設定値を含めていないか確認してください。

## 作業記録

改良内容と確認結果は[WORKLOG.md](./WORKLOG.md)に記録しています。
