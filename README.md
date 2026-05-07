# legal-docs

遠山和夫が個人で開発・配布するアプリのプライバシーポリシー・利用規約を集約したリポジトリ。

公開URL: <https://kazuotoyama.github.io/legal-docs/>

## 目的

- アプリごとに法務文書のリポジトリを作らず、ここで一元管理する
- Google Play Console / App Store Connect の各リリースから安定した公開URLを参照させる
- 連絡先メアド変更・改定時に1箇所直せば済む構造

## 構成

```
legal-docs/
├── _config.yml           # Jekyll 設定（GitHub Pages 用）
├── index.md              # トップページ（アプリ一覧）
├── rakusettei/           # らく設定
│   ├── privacy.md        # プライバシーポリシー
│   └── terms.md          # 利用規約
├── kanji-app/            # 漢字小学校
│   └── privacy.md
├── kanji-chu-app/        # 中学漢字練習帳
│   └── privacy.md
├── myphoto-slide-puzzle/ # マイフォト スライドパズル
│   ├── privacy.md
│   └── terms.md
├── fukushima-fishing/    # 潮よみ
│   └── privacy.md
├── gomidash/             # ゴミダッシュ
│   └── privacy.md
├── hachioji-gomi/        # 八王子市ゴミ出し検索
│   └── privacy.md
└── fujiyoshida-gomi/     # 富士吉田市ゴミ出し検索
    └── privacy.md
```

## 公開URLの命名規則

```
https://kazuotoyama.github.io/legal-docs/<app-slug>/<doc-type>/
```

例：
- `https://kazuotoyama.github.io/legal-docs/rakusettei/privacy/`
- `https://kazuotoyama.github.io/legal-docs/rakusettei/terms/`

## 新規アプリ追加手順

1. ルートに新しいディレクトリ作成（命名はケバブケース、例：`shioyomi/`）
2. `privacy.md`（必要なら `terms.md`）を配置
3. `index.md` のアプリ一覧に追記
4. コミット → プッシュ → 数分で公開URL反映

## 連絡先メアド変更時の手順

```bash
git grep -l "kazuotyama770@gmail.com" | xargs sed -i '' 's/kazuotyama770@gmail.com/<NEW_EMAIL>/g'
```

ただし、メアド変更は過去アプリのストア掲載情報・サポート連絡先すべてに影響するため、慎重に行うこと。
