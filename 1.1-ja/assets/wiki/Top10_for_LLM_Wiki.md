## Top10 for LLM (日本語版) Wiki

### 目的

このWikiページは、1.1-jaドラフト版作成プロジェクトの進捗状況をまとめたもので、プロジェクト・メンバー間の連携促進を目的としています。1.1-jaドラフト版翻訳・更新作業は、[このgithubレポジトリ](https://github.com/Setotet/Top10-for-LLM/tree/1.1-ja) 上で行っており、このWikiは、作業の進行に同期し最新の進捗状況を掲載しています。

OWASP Top 10 for Large Language Model Applications 全体の情報は、
[英語Wiki](https://owasp.org/www-project-top-10-for-large-language-model-applications/)に掲載されています。英語版PDFは、[このサイト](https://llmtop10.com/)でも公開しています。

### 進捗状況 - コミット毎の変更箇所

**翻訳・更新が行われると、新しいコミットが上に追加されていきます。**
| Changes in the commit | Commit message |
| ----------- | --------------------- |
| [R51205_223820](https://github.com/owasp-ja/Top10-for-LLM/commit/a86a0d5a6143aa1808aa78c3ac921f289f8f033f) | Initial changes to 1.1-ja/LLM01 to LLM10 (1.0-ja base) |
| [R51124_003440](https://github.com/owasp-ja/Top10-for-LLM/tree/1.1-ja/1.1-ja/1.0-ja_orig) | Base 1.0-ja |

### 進捗状況 - 全ての変更箇所と現在のBLEU score

**LLM-xx リンクをクッリクすると、github.comは全てのファイルを拡張表示します。注目のmdファイルまでスクロール・ダウンするか、または、左端の vマーク をクリックし、注目外のファイルを非表示にしてください。**
| Chapter title | All changes made so far | BLEU score |
| ------------- | --------------------- | ---------- |
| PromptInjection | [LLM-01](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9284 |
| InsecureOutputHandling | [LLM-02](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9615 |
| TrainingDataPoisoning | [LLM-03](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9505 |
| ModelDoS | [LLM-04](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9473 |
| SupplyChainVulnerabilities | [LLM-05](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9557 |
| SensitiveInformationDisclosure | [LLM-06](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9439 |
| InsecurePluginDesign | [LLM-07](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9456 |
| ExcessiveAgency | [LLM-08](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9769 |
| Overreliance | [LLM-09](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9604 |
| ModelTheft | [LLM-10](https://github.com/owasp-ja/Top10-for-LLM/compare/a86a0d5a6143aa1808aa78c3ac921f289f8f033f...main?diff=split) | 0.9563 |

### BLEU scoreについて

BLEU scoreは自然言語処理で広く用いられている2つの文章の類似度を示す 0.0~1.0 (inclusive) の小数で、1は完全に一致する、0は完全に異なることを意味します。日本語1.1版の作成は日本語1.0版をベースとし、英語の1.0版から1.1版への変更箇所に沿って、翻訳・更新していきますから、出発点ではベース（日本語1.0版）と完全一致、すなわち、BLEU scoreは1.0です。変更が進むにつれて減少していくので、日本語1.1版の翻訳・更新の進捗を表す一つの数値と解釈することができます。

しかし、0になることはありません。0.5以下になることもないでしょう。いくつになったら1.1版への更新作業が終了するかということを一意に定めることはできませんが、おおまかな目安として、[英語の1.0版から1.1版への更新](#英語版の10から11への更新)では、章ごとのBLEU scoreは0.54から0.90の間にあり、平均は0.7315です。英語版のBLEU scoreが小さい（変更が多い）章は日本語版でも小さくなる（翻訳・更新が多くなる）傾向を示すと思われます。

### BLEU scoreの変化

翻訳・更新は当該githubレポジトリへcommitすることで行っています。commit毎のBLEU scoreの実測値を示す経時折線グラフを以下に示します。

![BLEU scoreの変化](https://github.com/owasp-ja/Top10-for-LLM/tree/main/1.1-ja/assets/images/BLEU_Score.png)

### 英語版の1.0から1.1への更新

英語版は1.0と1.1が[このgithubレポジトリ](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications)にあります。英語版の1.0から1.1への変更は以下のようになっています。

| Chapter Title | Links to chapter diff | BLEU score |
| ------------- | --------------------- | ---------- |
| PromptInjection | [LLM-01](https://github.com/talesh/llm_top_ten_diffs/commit/f1ffe5cf96833fb15a585277996fd2cc05401396) | 0.7166 |
| InsecureOutputHandling | [LLM-02](https://github.com/talesh/llm_top_ten_diffs/commit/015539a321537a77cff3d5210b01b9d23ccba1d0) | 0.5495 |
| TrainingDataPoisoning | [LLM-03](https://github.com/talesh/llm_top_ten_diffs/commit/c1fa2664bf3dc078c458861fd45ac37d30953d00) | 0.5637 |
| ModelDoS | [LLM-04](https://github.com/talesh/llm_top_ten_diffs/commit/3d67a52b5d6962fb12ab9fbb4714ebdd2914f3b4) | 0.8589 |
| SupplyChainVulnerabilities | [LLM-05](https://github.com/talesh/llm_top_ten_diffs/commit/ff8f66336df56d27371c31da49c329f76937de13) | 0.6617 |
| SensitiveInformationDisclosure | [LLM-06](https://github.com/talesh/llm_top_ten_diffs/commit/96826c14f0fcf9ac0b8d85229349377eae9e27ff) | 0.7325 |
| InsecurePluginDesign | [LLM-07](https://github.com/talesh/llm_top_ten_diffs/commit/3742a4a4a246a3fec61dd110ec9ba921ff968d4f) | 0.7530 |
| ExcessiveAgency | [LLM-08](https://github.com/talesh/llm_top_ten_diffs/commit/9d0d60ecdf7901546b6c39e04618dcba22fafda9) | 0.8931 |
| Overreliance | [LLM-09](https://github.com/talesh/llm_top_ten_diffs/commit/3800d56c741d0c0df0759be36dbdfe50288e0b90) | 0.7547 |
| ModelTheft | [LLM-10](https://github.com/talesh/llm_top_ten_diffs/commit/6a2f97f85ccc20059f32e72535a2ee3bf6e94454) | 0.8309 |

### Reference Links

1. [Foundations of NLP Explained — Bleu Score and WER Metrics](https://towardsdatascience.com/foundations-of-nlp-explained-bleu-score-and-wer-metrics-1a5ba06d812b)
1. [BLEU Wikipedia](https://en.wikipedia.org/wiki/BLEU)
