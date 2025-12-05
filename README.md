# enhancer-evolution-poster-mbsj-2025
## 種横断エンハンサー予測AI：がん耐性・長寿動物に迫る新アプローチ

### 1. 背景：がん耐性・長寿動物の謎は「遺伝子調節」にある

1975年、イギリスの疫学者Petoはがんへのなりやすさと体の大きさが比例しないというパラドックスを提唱した。

一方で同年、海をはさんだアメリカで研究をしていたKing & Wilsonは、ヒトとチンパンジーの比較研究から「種差は遺伝子配列ではなく遺伝子調節に起因する」と提唱した。
それから40年の時が経った2015年、ゲノム解析が発達により、Villarらは哺乳類のエンハンサー・プロモーターの進化を調べた。この結果からエンハンサーが種特異的かつ、同じ日コード領域に存在するプロモーターと比較しても進化速度が大きい領域であることを示した。　
そこで我々は「がん耐性・長寿という極端な形質の鍵が、種特異的・種横断的なエンハンサーに存在する」という仮説を立てた。
  
しかし、これまでは非モデル生物のエンハンサーデータの不足などによりがん耐性・長寿動物のエンハンサー進化はほとんど調べられてこなかった。

### 2. 目的：エンハンサー進化解析の“壁”を超える AI の構築
データの不足を補うため、多種のゲノムからゲノムの文法を学習したDNA言語モデルをベースとした、エンハンサー予測AI 「EvoPhant」 を開発した。


### 3. 結果：EvoPhant は既存法を超え、種横断予測にも成功
① iEnhancer ベンチマークで既存法を上回る

特に EnhancerAtlas（豚・心臓）で高精度を示した

② ハダカデバネズミの H3k27ac由来のChIP-seq データでは性能低下
本データセットでは、エンハンサーを
H3K27ac − H3K4me3
のみで定義している。このことが影響した可能性があり、追加の実験による検証が必要

③ in vivo エンハンサー（ヒト/マウス）で種横断性能を検証（LOOSV）

ヒトで学習 → マウスで予測

マウスで学習 → ヒトで予測

ヒトデータで学習して、マウスのエンハンサー予測をしたときのほうが予測精度は高かった。また、予測疑陽性について、Encode Screeningで解析すると偽陽性ピークには近位エンハンサーが多く
存在しており、データセットに定義されていないcCREも捉えていた。

### 4. 今後：がん耐性・長寿の獲得機構を解明する新しい土台
本研究で開発したEvoPhantにより、がん耐性・長寿動物のエンハンサー進化に着目した仮説を検証するため、ATAC-seqなどWetの検証と統合する。



## A Cross-Species Enhancer Prediction AI: A New Approach to Cancer Resistance and Longevity
### 1. Background: The Mystery of Cancer Resistance and Longevity Lies in Gene Regulation

In 1975, the British epidemiologist Richard Peto proposed a paradox:
cancer incidence does not scale with body size or lifespan, despite the expectation that more cells and more cell divisions should increase cancer risk.

In the same year, across the ocean in the United States, King & Wilson proposed—based on human–chimpanzee comparisons—that
species differences arise not from protein-coding sequences, but from gene regulation.

Forty years later, with advances in genome-wide assays, Villar et al. (2015) analyzed multi-species ChIP-seq datasets and demonstrated that:

Enhancers are highly species-specific, and

They evolve more rapidly than promoters, even though both reside in non-coding regions.

Based on these findings, we hypothesized:
➡ Extreme traits such as cancer resistance and longevity may be encoded in species-specific enhancers.

However, due to limited sample availability in rare animals,
the evolution of enhancers in cancer-resistant and long-lived species has remained largely unexplored.

### 2. Objective: Building an AI System to Overcome the Barriers of Enhancer Evolution Analysis

To overcome data scarcity, we developed EvoPhant, an enhancer prediction AI model built upon a DNA language model that learns the “grammar” of genomes across diverse species.

### 3. Results: EvoPhant Outperforms Existing Methods and Enables Cross-Species Prediction
① Outperforms existing models on the iEnhancer benchmark

EvoPhant achieved particularly high accuracy on EnhancerAtlas (pig heart) datasets.

② Reduced performance on naked mole-rat H3K27ac-derived ChIP-seq data

This dataset defines enhancers using:

H3K27ac − H3K4me3

without incorporating H3K4me1, a typical enhancer mark.
This annotation difference may explain the reduced performance, and additional experimental validation is required.

③ Cross-species prediction validated using in vivo enhancers (human/mouse) with LOOSV

Trained on human → predicted mouse

Trained on mouse → predicted human

Models trained on human data showed higher accuracy when predicting mouse enhancers.

Furthermore, ENCODE Screening analysis of predicted false positives revealed:

Many corresponded to proximal enhancers, and

Some matched cCREs not included in the original dataset

→ suggesting that “false positives” often reflect biologically meaningful regulatory elements.

### 4. Future Directions: A New Foundation for Uncovering the Mechanisms of Cancer Resistance and Longevity

EvoPhant provides a computational foundation for studying enhancer evolution in rare species.
We will integrate this framework with ATAC-seq and other wet-lab validations to investigate the molecular mechanisms underlying cancer resistance and longevity.
