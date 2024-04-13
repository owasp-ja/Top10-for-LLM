## 第二章　LLM導入戦略の策定

大規模言語モデル（LLM）アプリケーションの急速な拡大により、業務で使用するあらゆるAI/MLシステム（生成AIと従来の予測AI/MLの両方）が注目され、評価される機運が高まっています。そのため、これまで見過ごされていたシステムを標的とする攻撃者や、法的、プライバシー、責任、保証の観点から軽視されていたガバナンスや法的課題などの潜在的なリスクが明らかになってきました。AI/MLシステムを業務に活用する組織にとって、包括的なポリシー、ガバナンス、セキュリティ・プロトコル、プライバシー対策、管理責任基準を評価・確立し、これらのテ技術が安全かつ倫理的にビジネス・プロセスと整合していることを確認することが重要です。

攻撃者（敵対者）は、企業、国民、政府機関にとって最も直接的で有害な脅威です。彼らの目的は、金銭的な利益からスパイ活動まで多岐にわたり、重要な情報を盗み、業務を妨害し、信用を傷つけることにあります。さらに、攻撃者は、AIや機械学習などの新技術を活用して手法を高度化し、攻撃のスピードを早めて防御が彼らの攻撃に先んじることを困難にしています。

多くの組織にとって差し迫ったLLMの脅威に、「シャドーAI」があります。「シャドーAI」とは、従業員が未承認のオンラインAIツールや安全でないブラウザのプラグインを使用したり、標準的なソフトウェアの承認プロセスを回避してアップデートやアップグレードすることによりLLM機能もつサードパーティのアプリケーションを使用している場合です。

>||center|16|16 LLM導入ステップ

>cornflower|white|left|14|18 ステップ 1: 強靭（きょうじん）であること

    >fidlightblue|black|justified|12|16 ▶ 脅威モデリングに基づいて直近の脅威を見つける
    >fidlightblue|black|justified|12|16 ▶ 脅威モデルシナリオにより内部・外部からの攻撃要因を見つけセキュリティ管理を確認する
    >fidlightblue|black|justified|12|16 ▶ 取り巻く環境を精査し、有名ブランドになりすます「ごろつきアプリ」を見つける

>dodgerblue|white|left|14|18 ステップ 2: 既存ポリシーを改定する

    >fidlightblue|black|justified|12|16 ▶ 契約、NDA、ガバナンス、セキュリティを見直し、LLM・生成AIの使用や脅威を加える

>fidblue|white|left|14|18 ステップ 3: トレーニングと教育

    >fidlightblue|black|justified|12|16 ▶ セキュリティのトレーニングや社員教育、開発・法務部門向けのトレーニングを改定し、LLM・生成AIの使用や脅威を加える

>darkblue|white|left|14|18 ステップ 4: 組織のリーダーを取り込む

    >fidlightblue|black|justified|12|16 ▶ 管理職、ビジネス・リーダーなど主だった役職に働きかけ、LLM・生成AIの解決戦略を定める
    >fidlightblue|black|justified|12|16 ▶ リスク回避戦略を実行する

>cornflower|white|left|14|18 ステップ 5: 第三者リスク管理施策を改定する

    >fidlightblue|black|justified|12|16 ▶ 第三者やベンダーが作成したAI機能に対して査察、精査が必要となる

>dodgerblue|white|left|14|18 ステップ 6: 導入戦略を策定する

##### 図 2.1　LLM導入ステップ
##### 　　作成 sdunn

### 導入戦略

LLMの適用範囲は、一般消費者向けのアプリケーションを活用するものから、個人データで独自のモデルをトレーニングするものまで多岐にわたります。利便性と統制の適切なバランスを決定するには、各々の場合、機密性の度合い、どの程度必要な機能か、それを決定するために利用可能なリソースのコストなどの要件を見極める必要があります。それら要件を見極めるための枠組みとして、5つの導入方法を以下に示します。

>||center|16|16 導入方法の種別

>cornflower|white|left|14|18 タイプ 1: 一般的な使用法を使う

    >fidlightblue|black|left|12|16 ▶ 大規模言語モデルを一般的な使用法でアクセスする
    >fidlightblue|black|left|12|16 ▶ 会社の方針を決め、従業員のトレーニングを行って、リスクを軽減する
    >fidlightblue|black|left|12|16 ▶ 利点：柔軟に、早く実験を進めることができる
    >fidlightblue|black|left|12|16 ▶ 例：Perplexity, ChatGPT, big-AGI

>dodgerblue|white|left|14|18 タイプ 2: モデルのAPIを経由してアクセスする

    >fidlightblue|black|left|12|16 ▶ ベンダー提供の大規模言語モデルのAPIを使いアクセスする
    >fidlightblue|black|left|12|16 ▶ 会社の方針を決め、従業員のトレーニングを行って、リスクを軽減する
    >fidlightblue|black|left|12|16 ▶ 利点：使用するAPIによりある程度の管理下で早く実験できる
    >fidlightblue|black|left|12|16 ▶ 例：Claude, ChatGPT, Gemini

>fidblue|white|left|14|18 タイプ 3: モデルをランセンスする

    >fidlightblue|black|left|12|16 ▶ エンタープライズ・クラスのサポート付きLLMをランセンスする
    >fidlightblue|black|left|12|16 ▶ 自社で管理しリスクを低減する。会社の方針を決め、従業員のトレーニングを行う。
    >fidlightblue|black|left|12|16 ▶ 利点：社内ツールやワーフローと統合し管理強化できる
    >fidlightblue|black|left|12|16 ▶ 例：Microsoft Enterprise CoPilot, Amazon Codewhisperer, SalesForce Einstein GPT

>darkblue|white|left|14|18 タイプ 4: 学習済みモデルを使う

    >fidlightblue|black|left|12|16 ▶ 自社データ、カスタムデータを使い基盤モデルを微調整する
    >fidlightblue|black|left|12|16 ▶ 透明性、機能性を増し、LLM幻覚を減らしてリスク低減する。会社の方針を決め、従業員のトレーニングを行う。
    >fidlightblue|black|left|12|16 ▶ 利点：機能強化、LLM幻覚を低減
    >fidlightblue|black|left|12|16 ▶ 例：QwenLM/Qwen 1.5, DBRX, Starling 7B

>cornflower|white|left|14|18 タイプ 5: 微調整済みモデルを使う

    >fidlightblue|black|left|12|16 ▶ 特別仕様のモデルを自社データを使い更に微調整する
    >fidlightblue|black|left|12|16 ▶ 透明性、機能性を増し、LLM幻覚を減らしてリスク低減する。会社の方針を決め、従業員のトレーニングを行う。
    >fidlightblue|black|left|12|16 ▶ 利点：一層のカスタマイズができる
    >fidlightblue|black|left|12|16 ▶ 例：Google MedPalm, Amazon Bedrock, Llama2, LegalAI

>dodgerblue|white|left|14|18 タイプ 6: モデルを自社開発する

    >fidlightblue|black|left|12|16 ▶ 自社仕様のAI/MLモデルを自社開発する
    >fidlightblue|black|left|12|16 ▶ 最高度の透明性と管理ができる。会社の方針を決め、開発者、従業員のトレーニングを行う。
    >fidlightblue|black|left|12|16 ▶ 利点：大きな投資が必要だが、高度な自社仕様

##### 図 2.2　導入方法の種別
##### 　　作成 sdunn
