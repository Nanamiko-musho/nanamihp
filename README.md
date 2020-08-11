# README
- https://rails-demo-1234.herokuapp.com/

## アプリ名

- Original HP & 日報管理

## 概要

- 零細企業(特に建築系)のHPと日報管理のオンライン化の為に作成

## 問題点 (ペルソナ)

- 自社のHPが無い
- 採用の窓口が無い
- 自社HPが無いので転職サイトに頼っている
- 日報などの業務管理を紙で行っている
- 営業や業務で一日中外回りをして日報を書く為だけに帰社する時間を無くす
- 社員の勤務時間外の時間を確保

## ゴール
- 零細企業のHP作成と日報管理のオンライン化
- 社員の勤務時間外の時間を確保
- 事務の書類業務と経費の削減
- 事務職員のリモートワーク化
- 採用をオンラインでの自社完結
- 非生産時間の削減

### 本番環境
- heroku

### 開発環境
- Cloud9

### 使用技術
- ruby
- Ruby on Rails
- HTML 
- CSS

### 課題や今後の実装にしたい機能

- 日報のCSV出力
- UIのデザインを強化すること
- 社員しか入れない様なログイン設定をすること
- 管理者権限をもつアカウント作成

### DB設計

#### users table

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string| null: false|
|password|string|null: false|

- devise 
:database_authenticatable, :registerable,:recoverable, :rememberable,:validatable
- has_many :posts

#### posts table

|Column|Type|Options|
|------|----|-------|
|constructionsite|text|null: false|
|writer|string|null: false|
|industrytype|string|null: false|
|members|string|null: false|
|comment|text|null: false|
|highway|string|null: false|
|endtime|string|null: false|
|overwork|string|null: false|
|travel_cost|string|null: false|
|user_id|integer|null: false|

- validates
:constructionsite,:writer,:industrytype,:members,:comment,:highway,:endtime,:overwork,:travel_cost, presence: true
- belongs_to :user
 

