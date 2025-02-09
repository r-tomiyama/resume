## 経歴概要

- 学生時代は Web サイト制作について独学で学び、複数の企業でWEBサイト制作のアルバイトを行った。
- 大学卒業後はインターネット広告代理店で、広告や CRM の分析/運用/コンサルティング業務に従事した。
- 入社数年後に自身の希望でアプリケーション開発部署へ異動。休暇も利用した自習・社内研修等を経て開発業務に携わる。
- 2~6 人のチームでフルスタックエンジニアとして業務用アプリケーションの開発を行う。 （バックエンド、静的型付け言語、設計が好き。インフラはやや苦手）

## スキル

### 言語

|    名前    |  年数  | 備考 |
| :--------: | :----: | :--: |
| JavaSript  |  6 年  |      |
| TypeScript |  4 年  |      |
|   Scala    |  2 年  |      |
|    Ruby    | 2 年 |      |
|   Python   |  1 年  |      |
|  Clojure   |  1 年  |      |
|    PHP     | 6 ヶ月 |      |
|    Elm     | 3 ヶ月 |      |

### フレームワーク

|     名前      |  年数  | 備考 |
| :-----------: | :----: | :--: |
| Ruby on Rails |  2 年  |      |
|    Vue.js     | 2 年半 |      |
|    Angular    | 2 年 |      |
|     React     | 2 年 |      |
| PlayFramwork  | 3 ヶ月 |      |

## 制作・開発職務の経歴

### 2023 年 9 月〜: シード期のスタートアップ

HR系のSaaS(中途採用者のオンボーディング管理ツール / 新卒採用管理システム)の開発に従事。  
Node.js, Express, Prisma, React, Firestore, PostgreSQL, Google Cloud (Firebase, Cloud Run, Cloud SQL, Cloud Tasks) など。  
開発フルタイムメンバー4人、業務委託メンバー1~7人の開発体制。

- 担当するプロジェクトに関する開発業務全般を行う。（要件定義、概念/用語の整理/共通認識化、詳細仕様の提案/擦り合わせ、設計、実装、レビュー、結合テスト項目の作成/実施）
- 日々、業務委託メンバーへのタスクアサインを担当する。（プロダクトオーナーと相談しながら、リファクタリングや細かい機能改善タスクの仕様/完了条件策定、優先度整理、各メンバーへのチケットの割り振り)
- ユニットテスト作成の推進
- 実施プロジェクト例
  - アカウント作成〜登録機能の仕様整理・統一（入力口によって仕様がまばらになってしまっていたため、既存仕様を解析。ばらつきがなくなるように機能をモジュール化して共有するなど）
  - Firestore から PostgreSQL への移行
  - シナリオ機能(ユーザー操作によってトリガーが発火し、あらかじめ設定したアクションを自動で予約実行する) の開発
  - 複数シナリオ機能（上述したシナリオを複数同時に利用できるようにするための改修。データ構造が変わり大きな改修となった）
  - tRPC の導入

### 2022 年 9 月〜 2023 年 9 月： 副業 (シード期のスタートアップ)

HR系のSaaS(中途採用者のオンボーディング管理ツール)の開発に従事。  
前述の通りのため省略。

### 2021 年 3 月〜 2022 年 3 月： 副業

初心者向けのプログラミングスクールで、メンター業務に従事。  
WEBアプリケーション開発の入門として HTML, CSS, Ruby, Ruby on Rails について教えた。

### 2019 年 4 月〜 2023 年 8月： [株式会社オプト](https://www.opt.ne.jp/)

インターネット広告代理店で、業務用アプリケーションの開発に従事。

#### 配信管理ツール

主な使用技術: Scala, Clojure, Python, JavaScript/Typescript, Vue.js, Terraform, AWS

- プロダクトリリース直前に開発チームに参加。Linter の整備や E2E テストの導入や機能追加などに携わった。
- 初めての本格的な開発業務だったが、幅広い技術をキャッチアップしながら取り組んだ。

#### [配信用広告データ作成ツール](https://tech-magazine.opt.ne.jp/entry/2022/04/22/141730)

主な使用技術: Scala, Sangria (sangria-graphql), Python, JavaScript/TypeScript, Vue.js, Terraform, AWS, GraphQL

- フロントエンドの初期設計・実装を主担当した。
  - Vue.js v2 with Composition API を採用。
  - GraphQL API をシンプルに利用できる Applo Client を採用。
  - Apollo CLI を利用して API のリクエスト・レスポンスの型をスキーマファイルから自動生成する仕組みを導入。
  - Jest で store が持つ振る舞いをユニットテストし、Cypress で E2E テスト を行う。

#### [広告データ作成ツール](https://tech-magazine.opt.ne.jp/entry/2022/04/15/150000)

主な使用技術: Ruby on Rails, JavaScript/TypeScript, Angular, GCP, AWS

- 負債が溜まって変更容易性が低いことが課題になっていたため、よく変更が入るコードを優先してリファクタリングを提案〜対応する。
  - まず、不足しているテストを実装する。テストコード実装を効率化するため、FactoryBot を導入する。
  - 同じバリデーション実装が入力口別に複数定義されていた問題の解消。入力口固有のバリデーションは残しておきつつ、Active Record の基本機能を利用したバリデーションに置き換える。
  - 広告データの種別を増やす際に、設定値を定義することで拡張できるように改善。ただし不正な設定値を定義した場合にはユニットテストで検知できるようにエラー処理を行う。
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

## その他

### 職務以外の開発経歴

あくまで余暇の趣味程度。

- Web ブラウザゲーム
  - [倉庫番](https://sisisin-soukoban.netlify.app/)（Elm, [github](https://github.com/sisisin-games/sisisin-soukoban)）
  - [PvP じゃんけん](https://peko-rock-paper-scissor.herokuapp.com/)（Node.js, [github](https://github.com/r-tomiyama/rock-paper-scissors)）
  - [8 pazzle](https://sisisin-8-pazzle.glitch.me/)（vite + React, [コード](https://glitch.com/edit/#!/sisisin-8-pazzle)）
- [シャッフルアプリ](https://shuffles.herokuapp.com/)（Ruby on Rails, [github](https://github.com/r-tomiyama/shuffles)）
- Slack 広告 Bot（Node.js, AWS(Lambda, API Gateway), Serverless Framework）

### 記事

あまり書けていない。

- Qiita: [@peko858](https://qiita.com/peko858)
- Zenn: [@peko858](https://zenn.dev/peko858)

## 自己 PR

- ステークホルダー内で認識を合わせるためのコミュニケーションが得意です。不明点は積極的に質問をしたり、進捗を分報などでこまめにライトに共有したり、言葉で伝わらない場合は簡易的でも図や資料を作ったりするなど、基本的なことを丁寧に行うことを意識しています。
- 主業務の周辺業務をタスクとしてアサインされずとも主体的に提案・進行することが得意です。（例： 日々のエラーチェックの体制・フローや機能開発後のQA依頼フローなどを作るなど）
- 保守性・拡張性を意識したコードを書くことやコンテナサービスを利用して環境間の差分がない状態で開発すること、 CI/CD を行うなど基本に則った開発ができます。
- 使ったことのない技術でも自立してキャッチアップすることが得意です。既存のプロダクトをコードリーディングして把握することはもちろん、取り扱ったことのない技術・ライブラリを調査し、導入することができます。
- 動的型付言語/静的型付言語、オブジェクト指向言語/関数型プログラミング言語を業務で利用したことがあり、Web アプリケーション開発でよく利用されるモダンな言語であればどの言語でもある程度利用することができます。
