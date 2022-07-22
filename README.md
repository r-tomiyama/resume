## 経歴概要

- 学生時代は Web サイト制作について独学で学び、複数の企業で制作のアルバイト行った。
- 大学卒業後はインターネット広告代理店で、広告や CRM の分析/運用/コンサルティング業務に従事した。
- 入社して 3 年目に自身の希望でアプリケーション開発部署へ異動。社内研修, OJT, 休暇も利用した自習を経て開発業務に携わる。
  - 2~6 人のチームで、（インフラはやや苦手だが）フルスタックエンジニアとして業務用アプリケーションの開発を行っている。

## スキル

### 言語

|    名前    |  年数  | 備考 |
| :--------: | :----: | :--: |
| JavaSript  |  5 年  |      |
| TypeScript |  3 年  |      |
|   Scala    |  3 年  |      |
|    Ruby    | 1 年半 |      |
|   Python   |  1 年  |      |
|  Clojure   |  1 年  |      |
|    PHP     | 6 ヶ月 |      |
|   jQuery   | 6 ヶ月 |      |
|    Elm     | 3 ヶ月 |      |

### 開発ツール・環境

|         名前         |  年数  | 備考 |
| :------------------: | :----: | :--: |
|     Git, Github      |  3 年  |      |
|        GitLab        | 6 ヶ月 |      |
|        ZenHub        | 6 ヶ月 |      |
|         Jira         | 6 ヶ月 |      |
|        Docker        |  3 年  |      |
|       CircleCI       |  3 年  |      |
|       Codecov        |  1 年  |      |
|      Coveralls       |  2 年  |      |
|         AWS          |  3 年  |      |
|         GCP          |  3 年  |      |
| アジャイル, スクラム | 1 年半 |      |

### フレームワーク

|     名前      |  年数  | 備考 |
| :-----------: | :----: | :--: |
| Ruby on Rails |  3 年  |      |
|    Vue.js     | 3 ヶ月 |      |
|    Angular    | 1 年半 |      |
|     React     | 3 ヶ月 |      |
| PlayFramwork  | 3 ヶ月 |      |

## 制作・開発職務の経歴

### 2021 年 3 月〜： 副業

初心者向けのプログラミングスクールで、メンター業務に従事。
主に HTML, CSS, Ruby, Ruby on Rails について教えている。

### 2019 年 4 月〜： [株式会社オプト](https://www.opt.ne.jp/)

インターネット広告代理店で、業務用アプリケーションの開発に従事。

#### 配信管理ツール

主な使用技術: Scala, Clojure, Python, JavaScript/Typescript, Vue.js, Terraform, AWS(ECS Fargate, Step Functions, Lambda, RDS (MySQL), S3, CloudWatch Events, CloudWatch Logs)

- プロダクトリリース直前に開発チームに参加。Linter の整備や E2E テストの導入や機能追加などに携わった。
- 初めての本格的な開発業務だったが、幅広い技術をキャッチアップしながら取り組んだ。

#### [配信用広告データ作成ツール](https://tech-magazine.opt.ne.jp/entry/2022/04/22/141730)

主な使用技術: Scala, Sangria (sangria-graphql), Python, JavaScript/TypeScript, Vue.js, Terraform, AWS（ECS Fargate, CloudFront, Lambda, RDS (MySQL), CloudWatch Logs）, GraphQL

- フロントエンドの初期設計・実装を主担当した。
  - Vue.js v2 with Composition API を採用。
  - GraphQL API をシンプルに利用できる Applo Client を採用。
  - Apollo CLI を利用して API のリクエスト・レスポンスの型をスキーマファイルから自動生成する仕組みを導入。
  - Jest で store が持つ振る舞いをユニットテストし、Cypress で E2E テスト を行う。
  - ESlint, Pretteir を利用した基本的な開発環境を用意。

#### [広告データ作成ツール](https://tech-magazine.opt.ne.jp/entry/2022/04/15/150000)

主な使用技術: Ruby on Rails, JavaScript/TypeScript, Angular, GCP(App Engine, Cloud SQL(MySQL), Cloud Pub/Sub, Cloud Logging, Cloud Storage), AWS(EC2, RDS(PostgreSQL), S3)

- 負債が溜まって変更容易性が低いことが課題になっていたため、よく変更が入るコードを優先してリファクタリングを提案〜対応する。
  - まず、不足しているテストを実装する。テストコード実装を効率化するため、FactoryBot を導入する。
  - 同じバリデーション実装が入力口別に複数定義されていた問題の解消。入力口固有のバリデーションは残しておきつつ、Active Record の基本機能を利用したバリデーションに置き換える。
  - 広告データの種別を増やす際に、設定値を定義することで拡張できるように改善。ただし不正な設定値を定義した場合にはユニットテストで検知できるようにエラー処理を行う。
  - 繰り返し利用されるフォーム実装やパーツをコンポーネント化する。
  - デッドコードや利用されていない機能を炙り出し掃除する。
- 広告素材ファイルアップロード機能のリプレイスを設計〜実装を主担当する。
  - 署名付き URL を利用して、API サーバを介さずにストレージへ直接ファイルをアップロードする。（API サーバを動かしている GAE ではアップロード可能な一時ファイルのサイズ制限が厳しく要件を満たせないため。また処理速度上の都合。
  - リアクティブフォームを利用したバリデーション実装を導入。

### 2015 年〜 2017 年： 学生時代のアルバイト

複数の会社でアルバイトとして、アプリ・Web サイト制作に携わった。
主な使用技術: PHP, WordPress, Javascript, jQuery, HTML, CSS

- マッチングサイトの制作（コーディング担当）
- テレビ番組の公式サイトのリニューアル制作（ディレクション, コーディング担当）
- アパレルメーカーの LP サイトの制作（コーディング担当）
- SNS アプリ開発（ディレクション担当）
- 不動産賃貸サイトの保守・運用
- 旅行代理店のツアーサイトの保守・運用

## その他、職務以外の開発経歴

- Web ブラウザゲーム
  - [倉庫番](https://sisisin-soukoban.netlify.app/)（Elm, [github](https://github.com/sisisin-games/sisisin-soukoban)）
  - [PvP じゃんけん](https://peko-rock-paper-scissor.herokuapp.com/)（Node.js, [github](https://github.com/r-tomiyama/rock-paper-scissors)）
  - [8 pazzle](https://sisisin-8-pazzle.glitch.me/)（vite + React）
- [シャッフルアプリ](https://shuffles.herokuapp.com/)（Ruby on Rails, [github](https://github.com/r-tomiyama/shuffles)）
- Slack 広告 Bot（Node.js, AWS(Lambda, API Gateway), Serverless Framework）

## 自己 PR

- 使ったことのない技術でも、自立してキャッチアップすることが得意です。
- TBD
