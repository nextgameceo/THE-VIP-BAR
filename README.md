# THE VIP BAR — 公式サイト

名古屋・栄の紹介制カラオケバー「THE VIP BAR」のランディングページです。

## 構成

```
.
├── index.html          # ページ本体（HTML / CSS / JS をすべて内包）
├── assets/
│   ├── logo.png        # 店舗ロゴ（透過PNG）
│   ├── ext_*.jpg       # 外観・看板・入口の写真
│   ├── room1.jpg       # 店内写真
│   ├── reina.jpg 他    # スタッフ写真
│   └── pay/            # 決済ブランドのロゴ（23種）
└── README.md
```

外部ライブラリは使っていません。Google Fonts のみ CDN から読み込んでいます。

## 公開方法

### GitHub Pages

1. このリポジトリを GitHub にプッシュ
2. リポジトリの **Settings → Pages** を開く
3. Source を `Deploy from a branch`、Branch を `main` / `(root)` に設定して保存
4. 数分後 `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます

### Vercel

1. [vercel.com](https://vercel.com) で **Add New → Project**
2. このリポジトリを選択
3. Framework Preset は `Other`、Build Command と Output Directory は空のままで **Deploy**

### Cloudflare Pages

1. Cloudflare ダッシュボード → **Workers & Pages → Create → Pages**
2. このリポジトリを接続
3. Build command は空、Build output directory は `/` を指定して **Save and Deploy**

## お問い合わせフォームの設定

`index.html` 内のフォームは、送信先が未設定の状態です。

```html
<form class="form rv" id="contactForm" action="" method="POST">
```

1. [Formspree](https://formspree.io) に無料登録し、新しいフォームを作成
2. 発行されたエンドポイント（`https://formspree.io/f/xxxxxxx`）をコピー
3. 上記の `action=""` に貼り付ける

```html
<form class="form rv" id="contactForm" action="https://formspree.io/f/xxxxxxx" method="POST">
```

これで送信内容が登録メールアドレスに届きます。無料プランは月50件までです。

## 内容の更新

| 更新したいもの | 場所 |
|---|---|
| 営業時間・定休日 | `index.html` の HERO と ACCESS セクション |
| メニュー・価格 | `index.html` の MENU セクション |
| スタッフ | `assets/` に写真を追加し、STAFF セクションに `<figure>` を追加 |
| 店内・外観の写真 | `assets/` を差し替え（INTERIOR は横スワイプ、枚数の増減も可） |
| SNS リンク | `index.html` 内の `instagram.com` / `tiktok.com` の URL |

## 注意

`assets/pay/` 内の各決済ブランドのロゴは、それぞれの企業の商標です。加盟店としての表示用途で使用しています。正式なブランド表示規定に沿った素材が必要な場合は、決済代理店（stera）から公式素材を取得して差し替えてください。
