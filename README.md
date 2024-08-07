# BoothEx

[BOOTH](https://booth.pm/ja)で販売されている3Dモデルの期間ごとの人気ランキングや検索機能を強化したサービスです。気に入った商品をフォルダ分けしたり、コーデ例として画像付きで公開できるようにする予定です。
ランキング上位商品はXに自動投稿される機能も実装予定です。

## 作りたい理由

- BOOTHの検索機能が不十分なため、自分が欲しい機能を持ったサイトを自分で作りたい。
- 3Dモデル市場が年々拡大しており、ユーザー数も見込める。

## ユーザー層

BOOTHでの3Dモデル購入層をターゲットとしています。

## 利用イメージ

- 現在の人気商品を手軽にチェックできる。
- ユーザー登録することで、欲しい商品をフォルダ分けできるようになる。
- 気になったフォルダをお気に入り登録できる。

## ユーザー獲得方法

- Qiitaに技術記事を公開する。
- 毎日のランキング上位商品をXに自動投稿する。
- 知人への紹介や配信での口コミを活用する。

## 差別化ポイント

- 検索機能を強化したサイトはあるが、スキ数の推移までを記録しているサイトは無い。

## 機能候補

### MVPリリース
- AWS Lambdaでの自動データスクレイピング
- 商品スキ数のデイリー・ウィークリーランキング表示
- タグ検索、ワード検索
- お気に入り商品のフォルダ分け
- Discordでのユーザー登録
- X botとの連携

### 本リリース
必要に応じて開発中に検討。

### その他アップデート案
- Lightテーマ
- ブロック機能

## 選定予定技術
- 全て無料枠で運用予定

- 開発環境 Docker
- バックエンド Cloudflare Pages Functions
- フロントエンド Remix
- デザイン TailwindCSS,shadcn/ui
- デプロイ Cloudflare Pages
- インフラ
   ・API: Amazon API Gateway  
   ・データ取得: AWS Lambda  
   ・ファイルサーバ: Cloudflare R2  
   ・データベースサーバ: Amazon DynamoDB  
- バージョン管理 GitHub
- CI/CD GitHubActions
- CMS Newt

## 画面遷移図
- Figma: https://www.figma.com/design/Xx1tCNx0belvOAJ2cOM4pq/BoothEX

## ER図
https://www.mermaidchart.com/raw/07177631-a5eb-4ee4-bacb-8e1d87d92ae2