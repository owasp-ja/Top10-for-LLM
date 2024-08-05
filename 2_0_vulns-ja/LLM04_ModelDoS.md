## LLM04: Model Denial of Service

### Description

攻撃者が非常に多くのリソースを消費する方法でLLMとやりとりすることで、自分自身や他のユーザーのサービス品質が低下し、さらには、高いリソースコストが発生する可能性があります。加えて、攻撃者がLLMのコンテキスト・ウィンドウを妨害、操作できてしまうことも、セキュリティ上の新たな懸念となっています。この問題は、様々なアプリケーションにおけるLLMの利用が増加し、リソースの集中的な利用が増えるとともに、ユーザーがどんな入力をするのか予測しにくいこと、更には、開発者の間でこのような脆弱性に対する一般的な認識が欠如していることなど、様々な背景から一層重要になっています。LLMでは、コンテキスト・ウィンドウは、入力と出力の両方をカバーする、モデルが管理できるテキストの最大長を表します。これはLLMの重要な特徴であり、モデルが理解できる言語パターンの複雑さと、任意の時点で処理できるテキストのサイズを決定します。コンテキスト・ウィンドウのサイズは、モデルのアーキテクチャによって定義され、モデルによって異なることがあります。

DoSの別の方法には、グリッチトークンが含まれます。グリッチトークンとは、モデルの処理を妨げ、一貫性のある応答を一部、または、全て出来なくしてしまう、ユニークで、問題を引き起こす文字列のことです。この脆弱性は、RAG(Retrieval-Augmented Generation, 正確で信頼性の高い情報を提供するために、データベースなど関連情報を検索・取得するなどし、LLMを使用する技術)がコラボレーションツールや文書管理システムなどの動的な内部リソースからデータを取得することが増えるにつれて悪化します。攻撃者は、これらのソースにグリッチトークンを挿入することによって、モデルの機能を損わせることでDoSを引き起こす可能性があります。

### Common Examples of Vulnerability

1.	キュー内のタスクを大量に生成し、リソースを繰り返し使用するようなクエリを送信します。(例.LangChainやAutoGPT 等)
2.	リソースを通常よりも多く消費するようなクエリを送信します。（例.通常とは異なる綴り方やシーケンスを使用等）
3.	継続的な入力オーバーフロー：攻撃者がLLMのコンテキスト・ウィンドウを超える入力を送信し、LLMに過剰な計算リソースを消費させるようにします。
4.	長い入力の繰り返し：攻撃者がLLMに対して、コンテキスト・ウィンドウを超えるような長い入力を繰り返し送信します。
5.	再帰的なコンテキスト展開：攻撃者が再帰的なコンテキスト拡張を引き起こす入力を構築し、LLMにコンテキスト・ウィンドウの拡張と処理を繰り返し行わせます。
6.	可変長入力フラッド：攻撃者がLLMに大量の可変長入力を送り、あふれさせます。このとき、各入力はコンテキスト・ウィンドウの限界にちょうど達するように注意深く作られます。このテクニックは、可変長入力の処理における非効率性を悪用し、LLMに負荷をかけ、応答不能にすることを目的としています。
7.	グリッチトークンRAGポイズニング：攻撃者がRAGのベクターデータベースのデータソースに対して、グリッチトークンを紛れ込ませます。その結果、RAGプロセスを通じて、これらの悪意のあるトークンがモデルのコンテキスト・ウィンドウに影響を与え、モデルが（部分的に）非論理的な結果を生み出すようになります。

### Prevention and Mitigation Strategies

1.	ユーザー入力が定義された制限に従い、悪意のあるコンテンツをすべてフィルタリングするように、入力の検証とサニタイズを実装します。
2.	リクエストやステップごとのリソース使用量を制限し、複雑な部分を含むリクエストの実行速度を遅くします。
3.	APIのレート制限を実施し、個々のユーザーまたはIPアドレスが特定の時間枠内で実行できるリクエスト数を制限します。
4.	キューに入れられたアクションの数と、LLMのレスポンスに反応するシステム内のアクションの総数を制限します。
5.	リソース利用を継続的に監視し、DoS攻撃を示す可能性のある異常なスパイクやパターンを特定します。
6.	過負荷とリソースの枯渇を防ぐため、LLMのコンテキスト・ウィンドウに基づく厳格な入力制限を設定します。
7.	LLMの潜在的なDoS脆弱性関する認識を、開発者の間で高め、安全なLLM実装のためのガイドラインを提供します。
8.	既知のグリッチトークンのリストを作成し、モデルのコンテキスト・ウィンドウに追加する前にRAGの出力をスキャンします。

### Example Attack Scenarios

1.	攻撃者が、ホストされたモデルに対して、困難でコストのかかる複数のリクエストを繰り返し送信することで、他のユーザーのサービス低下とホストのリソース利用の要求増加を引き起こします。
2.	LLMによって動いているツールが通常のクエリに応答するための情報を収集している間に、ツールは多くのウェブページリクエストを行い、大量のリソース消費を引き起こします。
3.	攻撃者がLLMのコンテキスト・ウィンドウを超える入力をLLMに継続的に送り続ける攻撃を仕掛けます。攻撃者は自動化されたスクリプトやツールを使って大量の入力を送信することで、LLMの処理能力に負荷をかけます。その結果、LLMは過剰な計算リソースを消費し、システムの著しい遅延、または、完全に応答できなくなってしまう状態を引き起こします。
4.	攻撃者は一連の連続した入力をLLMに送信し、各入力がコンテキスト・ウィンドウの限界にちょうど達するように設計されます。これらの入力を繰り返し送信することで、攻撃者は利用可能なコンテキストウィンドウの容量を使い果たすことを狙います。LLMがコンテキスト・ウィンドウ内でそれぞれの処理をしようとすると、システムリソースが逼迫し、パフォーマンスの低下や完全なDoSにつながる可能性があります。
5.	攻撃者はLLMの再帰的メカニズムを利用して、コンテキストの拡張を繰り返しトリガーさせます。LLMの再帰的な振る舞いを利用した入力を作成することで、攻撃者はモデルにコンテキスト・ウィンドウを繰り返し拡張して処理させ、大量の計算リソースを消費させます。この攻撃はシステムに負荷をかけ、DoS状態を引き起こし、LLMが応答しなくなったりクラッシュしたりすることがあります。
6.	攻撃者は、コンテキスト・ウィンドウの限界に近づくか、または、到達するように注意深く作成された、大量の可変長入力でLLMをあふれさせます。さまざまな長さの入力でLLMに負荷をかけることで、攻撃者は可変長入力の処理における非効率になることを利用しようとします。この入力により、LLMのリソースには過度な負荷がかかり、性能の低下を引き起こし、システムが通常のリクエストに応答する能力を妨げる可能性があります。
7.	DoS攻撃は一般的にシステムリソースを逼迫させることを目的としているが、APIの制限など、システムの振る舞いの他の側面から悪用することもあります。例えば、最近のSourcegraph社のセキュリティインシデントでは、悪意のあるアクターが漏洩した管理者アクセストークンを使用してAPIレート制限を変更し、異常なレベルでのリクエスト量を可能にすることで、サービスの中断を引き起こし得る状況にまで至りました。
8.	攻撃者がコラボレーションツールや文書管理ツールに既存の文書にグリッチトークンを追加するか、そのようなトークンを含む新しい文書を作成します。RAGのベクターデータベースが自動的に更新されると、これらの悪意のあるトークンが追加されます。LLMを通じて取得されると、これらのトークンは推論プロセスを攻撃し、LLMが非論理的な出力を生成する可能性があります。

### Reference Links

1. [LangChain max_iterations](https://twitter.com/hwchase17/status/1608467493877579777): **hwchase17 on Twitter**
2. [Sponge Examples: Energy-Latency Attacks on Neural Networks](https://arxiv.org/abs/2006.03463): **Arxiv White Paper**
3. [OWASP DOS Attack](https://owasp.org/www-community/attacks/Denial_of_Service): **OWASP**
4. [Learning From Machines: Know Thy Context](https://lukebechtel.com/blog/lfm-know-thy-context): **Luke Bechtel**
5. [Sourcegraph Security Incident on API Limits Manipulation and DoS Attack ](https://about.sourcegraph.com/blog/security-update-august-2023): **Sourcegraph**


## LLM04: Model Denial of Service

### Description

An attacker interacts with an LLM in a method that consumes an exceptionally high amount of resources, which results in a decline in the quality of service for them and other users, as well as potentially incurring high resource costs. Furthermore, an emerging major security concern is the possibility of an attacker interfering with or manipulating the context window of an LLM. This issue is becoming more critical due to the increasing use of LLMs in various applications, their intensive resource utilization, the unpredictability of user input, and a general unawareness among developers regarding this vulnerability. In LLMs, the context window represents the maximum length of text the model can manage, covering both input and output. It's a crucial characteristic of LLMs as it dictates the complexity of language patterns the model can understand and the size of the text it can process at any given time. The size of the context window is defined by the model's architecture and can differ between models.

An additional Denial of Service method involves glitch tokens — unique, problematic strings of characters that disrupt model processing, resulting in partial or complete failure to produce coherent responses. This vulnerability is magnified as RAGs increasingly source data from dynamic internal resources like collaboration tools and document management systems. Attackers can exploit this by inserting glitch tokens into these sources, thus trigger a Denial of Service by compromising the model's functionality.
Common Examples of Vulnerability

### Common Examples of Vulnerability

1. Posing queries that lead to recurring resource usage through high-volume generation of tasks in a queue, e.g. with LangChain or AutoGPT.
2. Sending unusually resource-consuming queries that use unusual orthography or sequences.
3. Continuous input overflow: An attacker sends a stream of input to the LLM that exceeds its context window, causing the model to consume excessive computational resources.
4. Repetitive long inputs: The attacker repeatedly sends long inputs to the LLM, each exceeding the context window.
5. Recursive context expansion: The attacker constructs input that triggers recursive context expansion, forcing the LLM to repeatedly expand and process the context window.
6. Variable-length input flood: The attacker floods the LLM with a large volume of variable-length inputs, where each input is carefully crafted to just reach the limit of the context window. This technique aims to exploit any inefficiencies in processing variable-length inputs, straining the LLM and potentially causing it to become unresponsive.
7. Glitch token RAG poisoning: The attacker introduces glitch tokens to the data sources of the RAGs vector database, thereby introducing these malicious tokens into the model's context window through the RAG process, causing the model to produce (partially) incoherent results.
Prevention and Mitigation Strategies

### Prevention and Mitigation Strategies

1. Implement input validation and sanitization to ensure user input adheres to defined limits and filters out any malicious content.
2. Cap resource use per request or step, so that requests involving complex parts execute more slowly.
3. Enforce API rate limits to restrict the number of requests an individual user or IP address can make within a specific timeframe.
4. Limit the number of queued actions and the number of total actions in a system reacting to LLM responses.
5. Continuously monitor the resource utilization of the LLM to identify abnormal spikes or patterns that may indicate a DoS attack.
6. Set strict input limits based on the LLM's context window to prevent overload and resource exhaustion.
7. Promote awareness among developers about potential DoS vulnerabilities in LLMs and provide guidelines for secure LLM implementation.
8. Build lists of known glitch tokens and scan RAG output before adding it to the model’s context window.

### Example Attack Scenarios

1. An attacker repeatedly sends multiple difficult and costly requests to a hosted model leading to worse service for other users and increased resource bills for the host.
2. A piece of text on a webpage is encountered while an LLM-driven tool is collecting information to respond to a benign query. This leads to the tool making many more web page requests, resulting in large amounts of resource consumption.
3. An attacker continuously bombards the LLM with input that exceeds its context window. The attacker may use automated scripts or tools to send a high volume of input, overwhelming the LLM's processing capabilities. As a result, the LLM consumes excessive computational resources, leading to a significant slowdown or complete unresponsiveness of the system.
4. An attacker sends a series of sequential inputs to the LLM, with each input designed to be just below the context window's limit. By repeatedly submitting these inputs, the attacker aims to exhaust the available context window capacity. As the LLM struggles to process each input within its context window, system resources become strained, potentially resulting in degraded performance or a complete denial of service.
5. An attacker leverages the LLM's recursive mechanisms to trigger context expansion repeatedly. By crafting input that exploits the recursive behavior of the LLM, the attacker forces the model to repeatedly expand and process the context window, consuming significant computational resources. This attack strains the system and may lead to a DoS condition, making the LLM unresponsive or causing it to crash.
6. An attacker floods the LLM with a large volume of variable-length inputs, carefully crafted to approach or reach the context window's limit. By overwhelming the LLM with inputs of varying lengths, the attacker aims to exploit any inefficiencies in processing variable-length inputs. This flood of inputs puts an excessive load on the LLM's resources, potentially causing performance degradation and hindering the system's ability to respond to legitimate requests.
7. While DoS attacks commonly aim to overwhelm system resources, they can also exploit other aspects of system behavior, such as API limitations. For example, in a recent Sourcegraph security incident, the malicious actor employed a leaked admin access token to alter API rate limits, thereby potentially causing service disruptions by enabling abnormal levels of request volumes.
8. An attacker adds glitch tokens to existing documents or creates new documents with such tokens in a collaboration or document management tool. If the RAGs vector database is automatically updated, these malicious tokens are added to its information store. Upon retrieval through the LLM these tokens glitch the inference process, potentially causing the LLM to generate incoherent output.

### Reference Links

1. [LangChain max_iterations](https://twitter.com/hwchase17/status/1608467493877579777): **hwchase17 on Twitter**
2. [Sponge Examples: Energy-Latency Attacks on Neural Networks](https://arxiv.org/abs/2006.03463): **Arxiv White Paper**
3. [OWASP DOS Attack](https://owasp.org/www-community/attacks/Denial_of_Service): **OWASP**
4. [Learning From Machines: Know Thy Context](https://lukebechtel.com/blog/lfm-know-thy-context): **Luke Bechtel**
5. [Sourcegraph Security Incident on API Limits Manipulation and DoS Attack ](https://about.sourcegraph.com/blog/security-update-august-2023): **Sourcegraph**
