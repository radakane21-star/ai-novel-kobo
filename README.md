# AI小説工房 — デプロイ手順

## 1. Firebaseの設定を貼り付ける

`index.html` の以下の部分を自分のFirebaseの設定に書き換える：

```js
const firebaseConfig = {
  apiKey: "REPLACE_WITH_YOUR_API_KEY",
  authDomain: "REPLACE_WITH_YOUR_AUTH_DOMAIN",
  ...
};
```

## 2. Firestoreのセキュリティルールを設定

Firebase Console → Firestore → ルール → `firestore.rules` の内容を貼り付けて公開

## 3. Vercelにデプロイ

```bash
# GitHubにpush
git init
git add .
git commit -m "AI小説工房"
git remote add origin https://github.com/あなた/ai-novel-kobo.git
git push -u origin main
```

Vercel (vercel.com) でGitHubリポジトリを接続 → 自動デプロイ完了

## 4. FirebaseのAuthorized domainsに追加

Firebase Console → Authentication → Settings → Authorized domains
→ VercelのURL（例: ai-novel-kobo.vercel.app）を追加

## 完成！
