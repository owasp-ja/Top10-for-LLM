## 第四章　LLM導入に役立つリソース

#### OWASP 大規模言語モデル・アプリケーション リスク トップ10

  >dodgerblue|white|left|12|16 LLM01: プロンプト・インジェクション
  >azure|black|justified|10|12 巧妙な入力によって大規模な言語モデル（LLM）を操作し、LLMが意図しない動作を引き起こします。システムのプロンプトを直接、上書きする手法、外部ソースからの入力を操作し、間接的に行う手法があります。

  >dodgerblue|white|left|12|16 LLM02: 安全が確認されていない出力ハンドリング
  >azure|black|justified|10|12 LLMの出力を細かくチェックせずにバックエンドシステムに送った場合、バックエンドの脆弱性をつかれ、意図しない結果を引き起こすことです。悪用されると、XSS、CSRF、SSRF、特権の昇格、リモート・コードの実行といった深刻な結果につながる可能性があります。

  >dodgerblue|white|left|12|16 LLM03: 訓練データの汚染
  >azure|black|justified|10|12 LLMの訓練データが改ざんされ、セキュリティ、有効性、倫理的行動を損なう脆弱性やバイアスなどが入り込むことです。訓練データの情報源として、Common Crawl、WebText、OpenWebText、書籍などが使われます。

  >dodgerblue|white|left|12|16 LLM04: モデルのDoS
  >azure|black|justified|10|12 LLMが計算リソースを大量に消費するようにしむけ、LLMを使ったサービスの品質低下や高コストを狙ったものです。

  >dodgerblue|white|left|12|16 LLM05: サプライチェーンの脆弱性
  >azure|black|justified|10|12 LLMアプリケーションが使用するコンポーネントやサービスの脆弱性によって引き起こされる攻撃です。サードパーティのデータセット、事前に訓練されたモデル、およびプラグインを使用することで脆弱性が増す可能性があります。

  >dodgerblue|white|left|12|16 LLM06: 機微情報の漏えい
  >azure|black|justified|10|12 LLMは、その応答の中に意図せず機密データを含めてしまう可能性があり、不正なデータアクセス、プライバシー侵害、セキュリティ侵害につながります。これを軽減するためには、データの浄化と厳格なユーザー・ポリシーを導入することが極めて重要です。

  >dodgerblue|white|left|12|16 LLM07: 安全が確認されていないプラグイン設計
  >azure|black|justified|10|12 LLMプラグインにおいて、入力の安全性が確認されておらず、あるいはアクセスコントロールが不十分な場合、悪意のあるリモート・コード実行のような結果をもたらす可能性があります。

  >dodgerblue|white|left|12|16 LLM08: 過剰な代理行為
  >azure|black|justified|10|12 この問題は、LLMベースのシステムに与えられた過剰な機能、権限、または自律性に起因し、意図しない結果を招くことがあります。

  >dodgerblue|white|left|12|16 LLM09: 過度の信頼
  >azure|black|justified|10|12 十分監督されていないLLMに過度に依存したシステムやユーザーは、LLMが生成したコンテンツが不正確または不適切なものであることに気づかず、誤った情報、誤ったコミュニケーション、法的問題、セキュリティの脆弱性に直面する可能性があります。

  >dodgerblue|white|left|12|16 LLM10: モデルの盗難
  >azure|black|justified|10|12 独自のLLMモデルへの不正アクセス、モデルのコピー、または流出が含まれます。その影響は、経済的損失、競争上の優位性の低下、機密情報へのアクセスの可能性などです。

##### 図 4.1　OWASP 大規模言語モデル・アプリケーション リスク トップ10
#### OWASP 大規模言語モデル・アプリケーション リスクの所在箇所
![OWASP Top10 for LLM Visual](images/GOV1_Fig_4_2_ja.png)
##### 図 4.2　OWASP 大規模言語モデル・アプリケーション リスクの所在箇所

### OWASPのリソース

LLMソリューションを導入すると、それまでになかった領域が攻撃対象となり、新たな課題が発生するため、特別な戦術や防御が必要になります。同時に、よく知られている問題と類似した問題も発生し、すでに確立されたサイバーセキュリティの手順と緩和策を適用することができる場合もあります。LLMサイバーセキュリティを、それらすでに確立されたサイバーセキュリティ管理、プロセス、手順と統合することで、脅威に対する脆弱性を減らすことができます。
これらがどのように統合されるかは、[OWASP Integration Standards（OWASP統合基準）](https://owasp.org/www-project-integration-standards/)をご覧ください。

#### OWASP リソース・リンク
  [OWASP SAMM](https://owasp.org/www-project-samm/)
#### 説明
  ソフトウェア保証成熟度モデル
#### お勧めする理由と使用方法
  効果的で組織の安全な開発ライフサイクルを分析し、改善するための測定可能な方法です。SAMMは、ソフトウェアライフサイクル全体をサポートします。SAMMはリスクを少しずつ絞り込む手法を取り、ソフトウエア開発におけるギャップを特定し、優先順位を付け、要点を絞って、セキュアな開発を可能にします。

#### OWASP リソース・リンク
  [OWASP AI Exchange](https://owasp.org/www-project-ai-security/)
  [OWASP 機械学習セキュリティ トップ10](https://mltop10.info/)
#### 説明
  OWASPのプロジェクトは、全世界でAIセキュリティを高め、標準化と相互協力を支援しています。
  OWASP AI ExchangeはOWASP AIセキュリティ・プライバシーガイドのための窓口です。
  OWASP 機械学習セキュリティ トップ10は、MLシステムのセキュリティの問題を対象にしています。
#### お勧めする理由と使用方法
  このプロジェクトは、ML Top 10 を含み、安全でプライバシーを保護するAIシステムの設計、作成、テスト、調達に関する明確で実行可能な施策を提供するため、常時、更新されている文書です。これは、AIのグローバルな規制とプライバシー情報のための最高のOWASPリソースです。

#### OWASP リソース・リンク
   Open Common Requirement Enumeration [OpenCRE](https://www.opencre.org/)
#### 説明
  OpenCRE (共通要件列挙)は、セキュリティ標準とガイドラインの両方を外観するためのプラットフォームで、少しずつ絞り込んでいくことができます。
#### お勧めする理由と使用方法
  標準、規格を検索するため。規格名またはコントロールタイプで検索できます。

#### OWASP リソース・リンク
  [OWASP脅威モデリング](https://owasp.org/www-community/Threat_Modeling)
#### 説明
  アプリケーションの脅威モデリングを行うための構造化された正式なプロセスです。
#### お勧めする理由と使用方法
  脅威モデリングについて広範な知識を得ることができます。アプリケーションのセキュリティに関する情報を体系的にまとめています。

#### OWASP リソース・リンク
  [OWASP CycloneDX](https://owasp.org/www-project-cyclonedx/)
#### 説明
  OWASP CycloneDXは、サイバーリスク低減のための高度なサプライチェーン機能を提供するフルスタックの部品表（BOM）規格です。
#### お勧めする理由と使用方法
  ソフトウェアはサードパーティやオープンソースのコンポーネントを使用することが多くなっています。これらのコンポーネントは、複雑でそれぞれの用途に応じて異なった方法で使われ、目的とする機能を実現します。SBOM（Software Bill of Materials）は、リスクを特定し、透明性を高め、迅速な影響分析を可能にする、すべてのコンポーネントの正確な部品表です。
  [EO 14028](https://www.nist.gov/itl/executive-order-14028-improving-nations-cybersecurity/software-security-supply-chains-software-1) は、米国連邦政府システムのSBOMに関する最低要件を規定しています。

#### OWASP リソース・リンク
  [OWASP ソフトウェアコンポーネント検証規格（SCVS）](https://scvs.owasp.org/)
#### 説明
  アクティビティ、コントロール、ベストプラクティスを作成するためのフレームワークを確立するコミュニティ主導の取り組みです。
#### お勧めする理由と使用方法
  ソフトウェアサプライチェーンのリスクを減らし、さらに進んだソフトウェア・サプライチェーン管理を実現するための施策、管理、最善の対処法を策定するのに役立ちます。

#### OWASP リソース・リンク
  [OWASP API セキュリティ プロジェクト](https://owasp.org/www-project-api-security/)
#### 説明
  アプリケーション・プログラミング・インターフェース（API）のセキュリティに関するユニークな脆弱性とセキュリティリスクを理解し、軽減するための戦略とソリューションについて説明しています。
#### お勧めする理由と使用方法
  アプリケーションはAPIを経由して接続されています。ユーザと組織を保護するためには、APIの誤設定や脆弱性を減らすことが必須です。ビルド環境と製品環境のセキュリティテストとレッドチームに使用することができます。

#### OWASP リソース・リンク
  [OWASP Top 10 CI/CD セキュリティ リスク](https://owasp.org/www-project-top-10-ci-cd-security-risks/)
#### 説明
  継続的インテグレーションと高い頻度の自動デプロイのセキュリティのための要点を示しています。
#### お勧めする理由と使用方法
  開発者の手から製品環境まで、ソフトウエアをデプロイするプロセスのセキュリティを高めるために役立ちます。ビルド環境と製品環境のセキュリティテストとレッドチームに使用することができます。

#### OWASP リソース・リンク
  [OWASP アプリケーション セキュリティ 検証基準 ASVS](https://owasp.org/www-project-application-security-verification-standard/)
#### 説明
  アプリケーション・セキュリティ検証標準（ASVS）は、ウェブアプリケーションの技術的なセキュリティ管理をテストするための基礎を提供し、また、開発者に安全な開発のための要求事項のリストを提供します。
#### お勧めする理由と使用方法
  ウェブアプリケーション用セキュリティ要件、セキュリティテスト、一覧表を作成するのに使用します。様々なアプリケーションの使い道、ユーザーの流れに沿ったリリース・テストを確立するために役立ちます。

#### OWASP リソース・リンク
  [OWASP 脅威およびセーフガードマトリックス (TaSM)](https://owasp.org/www-project-threat-and-safeguard-matrix/)
#### 説明
  ビジネスを守るために、すぐに適用可能な方策を示す一覧を提供します。
#### お勧めする理由と使用方法
  この一覧により、主要な脅威をNISTサイバーセキュリティフレームワークの機能（特定、保護、検知、対応、回復）に重ね合わせ、強固なセキュリティ計画を構築することができます。組織全体のセキュリティを追跡し、報告するダッシュボードとして使用できます。

#### OWASP リソース・リンク
   [欠陥 道場](https://www.defectdojo.com/)
#### 説明
  オープンソースの脆弱性管理ツールで、テンプレート化、レポート作成、数値化により、テストプロセスを合理化します。使用例を示すツールも用意されています。
#### お勧めする理由と使用方法
  「欠陥 道場」を使えば、テンプレートを使い、一般的な脆弱性を検出し、レポート生成、数値化し、脆弱性のログ作成時間を短縮できます。

### MITREのリソース

LLM の脅威が頻発するようになったことで、攻撃対象領域を防御するために「強靭さ第一」の価値が再認識されてきています。従来のTTPS（註1）は、LLMにおける新たな攻撃対象領域と機能を取り込んでいます。MITREは、実際に起こった例に基づいて攻撃者の戦術と手順を理解するために、確立され広く受け入れられている枠組みを使っています。

【註】
1. TTPS：Tactics, Techniques, and Procedures
攻撃者がサイバー攻撃を仕掛ける際にとる行動、戦術、手順を記述したもの

組織のLLMセキュリティ戦略に、 MITRE ATT&CK と MITRE ATLAS を適用することで、LLMセキュリティが現在のAPIセキュリティ標準などのプロセスでカバーされている部分、カバーされていない部分を特定することができます。

MITRE ATT&CK（Adversarial Tactics, Techniques, and Common Knowledge）は、MITRE Corporationによって作成されたフレームワーク、データマトリックス集、および評価ツールで、世界中で使用されている知識リポジトリです。MITRE ATT&CKマトリックスは、攻撃者が特定の目標を達成するために使用する戦略集を含んでおり、これらの目的は戦術ごとに分類されています。さらに、攻撃順に示されており、偵察（reconnaissance）から始まり、最終的な目標である殲滅（exfiltration）または破壊（impact）へと進んでいきます。

MITRE ATLASは「Adversarial Threat Landscape for Artificial Intelligence Systems」の略で、悪質な行為者による機械学習（ML）システムへの攻撃の実例に基づいた知識ベースです。ATLASはMITREのATT&CKアーキテクチャに基づいており、その戦術と手順はATT&CKを補完するものです。

#### MITRE リソース・リンク
  [MITRE ATT&CK](https://attack.mitre.org/)
#### 説明
  実際の観察に基づく攻撃者の戦術とテクニックの知識ベース
#### お勧めする理由と使用方法
  具体的な脅威モデルと方法論の開発の基礎として使用します。組織内の既存の管理策を攻撃者の戦術や技法に照らし合わせ、抜けている部分やテストすべき領域を特定します。

#### MITRE リソース・リンク
  [MITRE AT&CK 作業台](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/attck-workbench/)
#### 説明
  ローカルな知識ベースを使って、ATT&CKの作成または拡張する際に使うツールです。
#### お勧めする理由と使用方法
  ATT&CK 知識ベースをコピーし、新しい、または更新されたテクニック、戦術、緩和策グループ、および組織に特化したソフトウェアで拡張することができます。

#### MITRE リソース・リンク
   [MITRE ATLAS](https://atlas.mitre.org/)
#### 説明
  MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) は、攻撃戦術や攻撃手法をMLに特化した知識ベースです。実例やレッドチーム・セキュリティチームによるデモ、研究者の挙げた可能な手法が網羅されています。
#### お勧めする理由と使用方法
  すでに知られているML特有の脆弱性を知ることができます。

#### MITRE リソース・リンク
  [MITRE ATT&CK Powered Suit](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/attack-powered-suit/)
#### 説明
  ATT&CK Powered Suit は、MITRE ATT&CK知識ベースをあなたの手元に置くブラウザ拡張機能です。
#### お勧めする理由と使用方法
  ワークフローを中断することなく戦術、テクニックなどを検索することができます。

#### MITRE リソース・リンク
  [The Threat Report ATT&CK Mapper (TRAM)](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/threat-report-attck-mapper-tram/)
#### 説明
  CTI(Cyber Threat Intelligence)レポートのTTP(tactics,techniques,procedures)検索を自動化します。
#### お勧めする理由と使用方法
  CTIレポートに見られるTTPをMITRE ATT&CKに対応させる手順は、エラーが発生しやすく、時間がかかります。TRAMはLLMを使用し、最も一般的な50のテクニックについてこのプロセスを自動化します。Juypterノートブックも用意されています。

#### MITRE リソース・リンク
   [Attack Flow v2.1.0](https://center-for-threat-informed-defense.github.io/attack-flow/)
#### 説明
  アタックフローはサイバー攻撃者が、様々な攻撃技術をどのように組み合わせ、目的を達成するのかを記述するための言語です。
#### お勧めする理由と使用方法
  攻撃者がどのようなテクニックを使うかを理解することで、防御者は敵の動きを理解し、自らの防御態勢を向上させることができます。

#### MITRE リソース・リンク
  [MITRE カルデラ](https://caldera.mitre.org/)
  [Caldera 用のプラグイン](https://caldera.readthedocs.io/en/latest/Plugin-library.html) 
#### 説明
  攻撃者の動きをシミュレートし、対するレッドチームを支援し、インシデント応答を自動化するように設計された、サイバーセキュリティ・プラットフォームです。
#### お勧めする理由と使用方法（プラグインへのリンク付）
  プラットフォームのコア機能を拡張し、エージェント、レポート、TTP のコレクションなどの追加機能を提供するプラグインも用意されていま。

#### MITRE リソース・リンク
  [CALDERA ラグイン: アーセナル](https://www.mitre.org/news-insights/news-release/microsoft-and-mitre-create-tool-help-security-teams-prepare-attacks)
#### 説明
  AI対応システムへの攻撃者をシミュレートするプラグインです。
#### お勧めする理由と使用方法
  このプラグインは、CALDERA とインターフェースするため、MITRE ATLAS に定義されたTTP を提供します。

#### MITRE リソース・リンク
  [アトミック・レッド・チーム](https://github.com/redcanaryco/atomic-red-team)
#### 説明
  MITRE ATT&CKフレームワークで使う、攻撃者をシミュレートするテストのライブラリです。
#### お勧めする理由と使用方法
  コントロールの検証とテストのために使用することができます。セキュリティチームは、Atomic Red Teamを使用することで、自分たちの環境を素早く、ポータブルに、再現性よくテストすることができます。アトミックテストはコマンドラインから直接実行できます。

#### MITRE リソース・リンク
  [MITRE CTI ブループリント](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/cti-blueprints/)
#### 説明
  サイバー脅威情報のレポートを自動化します。
#### お勧めする理由と使用方法
  CTIブループリントは、サイバー脅威インテリジェンス（CTI）アナリストが、高品質で実用的なレポートを効率的な作成を支援します。

### AI脆弱性リポジトリ

#### 名称
  [AI インシデント・データベース](https://incidentdatabase.ai/)
#### 説明
  過去に失敗したAIアプリケーションの事例を蓄積しています。大学の研究グループによって維持され、クラウドソーシングされています。

#### 名称
  [OECD AI インシデント・モニター (AIM)](https://oecd.ai/en/incidents)
#### 説明
  AIに関連する課題を理解するためのわかりやすい出発点を提供します。

### AIモデルの脆弱性を追跡する企業

1. [Huntrバグバウンティ：プロテクトAI](https://huntr.com/)
  AI/ML向けバグ報奨金プラットフォーム
2. [AI脆弱性データベース(AVID)：ガラク](https://avidml.gitbook.io/)
  モデルの脆弱性データベース
3. [AIリスクデータベース：ロバスト・インテリジェンス](https://airisk.io/)
  モデルの脆弱性データベース
4. [LVE Repository](https://lve-project.org/blog/launching-the-lve-project.html)
  オープン LLM Vulnerability and Exposures レポジトリ

### AI調達ガイダンス

#### 名称
  [世界経済フォーラム：AI責任の導入：民間セクターによるAIソリューション調達のためのガイドライン：インサイトレポート 2023年6月](https://www.weforum.org/publications/adopting-ai-responsibly-guidelines-for-procurement-of-ai-solutions-by-the-private-sector/)
#### 説明
  AIシステムの調達のための、標準ベンチマークと評価基準は、まだ開発初期段階にあります。この調達ガイドラインは、エンド・ツー・エンドの調達プロセスにおける考慮事項の基準を提供しています。このガイダンスを使うと、既存の「サードパーティ・リスク・サプライヤーとベンダー調達プロセス」を強化することができます。
