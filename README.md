■サービス概要  
[BOOTH](https://booth.pm/ja)で販売されている3Dモデルの期間ごとのお気に入りランキングや、検索機能を強化したサイト  
気に入った商品をフォルダ毎に管理したり、コーデ例として公開できるようにする  
ランキング上位商品をXに自動ポストする  
  
■ このサービスへの思い・作りたい理由  
Boothの検索機能が弱く、自分が今商品を探す時に新着順でポチポチ次を押していくか、最近公開された商品かつ人気順でソートぐらいしか出来ないので、自分が欲しいと思った機能を持ったサイトを作りたい。  
3Dモデル市場は年々大きくなってきており、サイト利用者数も見込める。*参考[BOOTHの3Dモデル販売は30億円突破 販売数200万件に迫る](https://www.watch.impress.co.jp/docs/news/1565599.html)  
  
■ ユーザー層について  
3Dモデル購入層をそのまま抱き込みたい。  
  
■サービスの利用イメージ  
今の人気商品を手軽に知る事が出来る。  
ユーザー登録する事で購入予定だったり欲しいと思っている商品をフォルダ分け出来る。  
  
■ ユーザーの獲得について  
初動はQiitaに技術記事を公開。
毎日ランキング上位商品をXに自動ポストする。  
知人への紹介や配信での口コミ。  
  
■ サービスの差別化ポイント・推しポイント  
スキ数でのランキングまで作っているサイトは無い。  
既にある日本語の競合するであろうサイトはUI/UXが少し悪い。  
  
■ 機能候補  
・MVPリリース  
AWS Lambdaでの自動データスクレイピング機能  
商品スキ数のデイリーランキング、ウィークリーランキングの表示機能  
タグ検索、ワード検索  
お気に入り商品のフォルダ分け機能  
Discordでのユーザー登録機能  
X botとの連携  
・本リリース  
実際に作りながら必要だと感じたら追加  
・アップデート  
Lightテーマ  
  
■ 機能の実装方針予定  
全て無料枠で収める  
インフラはAWSを利用  
動的機能についてはAWS Lambdaで実装  
Amazon RDSは無料期間が12ヶ月なのでDynamoDBを使う  
デプロイ先は無料枠があり、バックエンド機能とも連携が出来るCloudflare  
Cloudflare Pages FunctionsとAWSと連携させる  
  
・現時点での選定技術  
■ 開発環境: Docker  
■ サーバサイド: Cloudflare Pages Functions  
■ フロントエンド: Remix  
■ CSSフレームワーク: TailwindCSS,shadcn/ui  
■ インフラ:  
・ API:Amazon API Gateway  
・ データ取得: AWS Lambda  
・ Webアプリケーションサーバ: Cloudflare Pages  
・ ファイルサーバ: Cloudflare R2  
・ データベースサーバ: Amazon DynamoDB(無料で運用する為)  
■ その他：  
・ VCS: GitHub  
・ CI/CD: GitHubActions  