# andsalon.com（*&salon lesson の公式サイト）

静的な HTML だけ。`/terms`（利用規約）と `/privacy`（プライバシーポリシー）は App Store の審査員とアプリ内のリンクが開く。

## 公開のしかた（SaronBook の LP と同じ Vercel）
1. このフォルダを GitHub の新しいリポジトリ（例 `andsalon-site`）に push する（`site/` の中身をルートに）。
2. Vercel で「Add New Project」→ そのリポジトリを選ぶ → Framework は Other、Build なし → Deploy。
3. Vercel の Project → Settings → Domains に `andsalon.com` と `www.andsalon.com` を追加し、
   表示される DNS 設定（A レコード `76.76.21.21` / CNAME `cname.vercel-dns.com`）をドメインの管理画面に入れる。
4. `https://andsalon.com/terms` と `https://andsalon.com/privacy` が開けたら、アプリ（`login_screen.dart` の `termsUrl` / `privacyUrl`）
   と ASC（`tool/asc_listing.py apply` の `PRIVACY_URL` / `SUPPORT_URL`）は既にこの URL を指している。

## 文面を変えるとき
- 規約・ポリシーの正本はこの 2 ファイル。App Review 1.2（UGC）のため、**不適切な内容への「一切許容しない」「原則 24 時間以内に対応」**の文言と、
  報告のやり方（メッセージを長押し → メニューの「報告」）は消さない。
- 料金・紹介割引の説明は `docs/APP_STORE_LISTING.md` の決定と合わせる。
