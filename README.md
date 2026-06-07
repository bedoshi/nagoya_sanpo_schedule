# nagoya_sanpo_map

名古屋 2泊3日（金山発着）のさんぽマップをまとめた静的サイトです。
マスト9スポットを金・土の2日間に集約し、両日とも金山駅に帰着する動線で構成しています。

## 内容

- `index.html` — サイト本体（単一ファイル・依存なし）。各スポットからGoogleマップへのリンク付き。

## ローカルで確認する

```bash
# このフォルダで
python3 -m http.server 8000
# ブラウザで http://localhost:8000 を開く
```

または `index.html` をダブルクリックで開くだけでも表示できます。

## GitHub にリポジトリを作って公開する手順

ローカルにこのフォルダ（`index.html` と `README.md`）を置いた状態で:

```bash
cd nagoya_sanpo_map
git init
git add .
git commit -m "Add Nagoya sanpo map site"
git branch -M main

# GitHub 側でリポジトリ "nagoya_sanpo_map" を作成してから:
git remote add origin https://github.com/<あなたのユーザー名>/nagoya_sanpo_map.git
git push -u origin main
```

GitHub CLI が入っていれば、リポジトリ作成〜push まで一括でできます:

```bash
cd nagoya_sanpo_map
git init && git add . && git commit -m "Add Nagoya sanpo map site"
gh repo create nagoya_sanpo_map --public --source=. --push
```

### GitHub Pages で公開

1. リポジトリの **Settings → Pages** を開く
2. **Build and deployment → Source** を `Deploy from a branch` に設定
3. Branch を `main` / `/ (root)` にして Save
4. 数分後、`https://<ユーザー名>.github.io/nagoya_sanpo_map/` で公開されます

## メモ

- 営業時間・休館日は変動の可能性があります。訪問前に各店舗・施設の最新情報をご確認ください。
- 名古屋港ポートビルは月曜休館（今回の日程では日曜が帰路日のため影響なし）。
