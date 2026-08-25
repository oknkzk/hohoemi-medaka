# ほほえみめだか ホームページ

`index.html` と `style.css` だけのシンプルな1ページサイトです。
無料・独自ドメイン不要で GitHub Pages に公開できます。

## 中身の編集

`index.html` 内の `<!-- ▼〜書き換えてください -->` というコメントの
下にある部分を書き換えれば内容が変わります。編集箇所は以下の5つです。

1. 店名・キャッチコピー（ページ上部）
2. お店の説明文
3. お知らせ（`<li>` をコピーして増やしてください。新しいものを上に）
4. 住所・販売場所・Googleマップの埋め込み
   - Googleマップでお店の場所を検索 →「共有」→「地図を埋め込む」
   - 表示された `<iframe ...>` タグの `src="..."` の値だけをコピーして、
     `index.html` 内の `<iframe src="">` に貼り付けてください
5. Instagramのリンク先URL

デザイン（色味）を変えたい場合は `style.css` の一番上、`:root { ... }` の
中の色コード（`--color-primary` など）を変えるだけで全体に反映されます。

## GitHub Pages での公開手順

GitHubアカウントをお持ちとのことなので、下記の手順で公開できます。

1. GitHubで新しいリポジトリを作成する（例: `medaka-shop`）
2. このフォルダの中身（`index.html` / `style.css` / このREADME）を
   リポジトリに追加して push する

   ```bash
   git init
   git add .
   git commit -m "first commit"
   git branch -M main
   git remote add origin https://github.com/Okazuuu/hohoemi-medaka.git
   git push -u origin main
   ```

3. GitHub上でリポジトリの `Settings` → `Pages` を開く
4. `Build and deployment` の `Source` を `Deploy from a branch` にし、
   Branch を `main` / `/(root)` にして `Save`
5. 数十秒〜数分待つと、`https://Okazuuu.github.io/hohoemi-medaka/`
   でページが公開されます（Settings → Pages の画面にURLが表示されます）

## 更新のしかた

内容を直したくなったら、`index.html` などを編集して

```bash
git add .
git commit -m "お知らせを更新"
git push
```

とするだけで、数十秒〜1分程度で公開ページに反映されます。
