# WagyuMate 再開メモ

更新日: 2026-09-25 (日本時間)

## 作業対象

- 作業フォルダ: `C:\Users\200ca\WagyuMate-work`
- 元プロジェクト: `C:\Users\200ca\wagyu-mate`。次回の改良はそちらではなく、作業フォルダで続ける。
- 最新の共有用 ZIP: `C:\Users\200ca\WagyuMate-work\WagyuMate-fixed.zip`

## 今日の変更

- `utils/receiptParser.ts`: 伝票OCRの価格抽出を修正。桁区切りの価格を優先し、席番号や日齢などを価格として拾う誤認を避ける。ラベル付き価格は低額でも採用し、ラベルが読み取れない場合は10万円以上の桁区切り金額に限定する。
- `components/ReceiptScanner.tsx`: 生年月日と開催日を令和固定で表示して負の年のように見せていたため、西暦で確認・修正できる入力に変更。
- `WagyuMate-fixed.zip` を作成。ソース、設定、README、ロックファイルを含み、`node_modules` と `dist` は除外。

## 確認状況

- `node_modules\\.bin\\tsc.cmd --noEmit`: 成功。
- `npm.cmd run build`: 成功。500 kB を超える JS チャンクの警告あり。
- パーサーの入力例で、個体識別番号・生年月日 `2007-10-28`・開催日 `2008-08-17`・価格 `804000` の抽出を確認。
- 元画像をブラウザに読み込ませた一連のOCR操作は未確認。次回はアプリ上で伝票画像を再スキャンし、日付・価格が確認画面と保存後の個体詳細の両方で正しいことを確認する。

## 次回の再開手順

1. `C:\Users\200ca\WagyuMate-work` を開く。
2. `SESSION-RESUME.md` と `WORKLOG.md` を確認する。
3. 実伝票画像で OCR と保存後の値を確認し、誤認があればパーサーを調整する。
