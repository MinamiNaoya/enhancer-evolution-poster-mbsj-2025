# enhancer-evolution-poster-mbsj-2025
## 種横断エンハンサー予測AI：がん耐性・長寿動物に迫る新アプローチ

### 1. 背景：がん耐性・長寿動物の謎は「遺伝子調節」にある

大型・長寿にもかかわらず低いがん発生率を示すゾウ・ホッキョククジラは、Petoのパラドックスとして知られる生物学上の未解決問題である。

一方で King & Wilson（1975）は、「種差は遺伝子配列ではなく遺伝子調節に起因する」と提唱し、
Villar らは多種比較で エンハンサーが最も高速に進化する領域であることを示した。

➡ がん耐性・長寿という極端な形質の鍵が、種特異的エンハンサーに存在する可能性がある。

しかし、希少動物ではサンプル取得が難しく、エンハンサー解析は長年停滞していた。

### 2. 目的：エンハンサー進化解析の“壁”を超える AI の構築

がん耐性・長寿動物における
「エンハンサーの種横断予測」
を可能にするため、DNA言語モデルを基盤とした新規AI EvoPhant を開発した。


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



## Cross-Species Enhancer Prediction AI: A New Approach to Uncover Cancer Resistance and Longevity in Animals
### 1. Background: The mystery of cancer-resistant, long-lived animals lies in gene regulation

Elephants and bowhead whales exhibit remarkably low cancer incidence despite their large body size and long lifespan—a long-standing biological paradox known as Peto’s paradox.

King & Wilson (1975) proposed that phenotypic differences among species arise primarily from changes in gene regulation rather than coding sequences.
Villar et al. further showed through multi-species comparisons that enhancers are among the fastest-evolving regions in the genome.

➡ These findings suggest that the key to extreme phenotypes such as cancer resistance and extended longevity may lie in species-specific enhancer evolution.

However, enhancer studies in rare or non-model species have been limited due to difficulties in sample acquisition.

### 2. Objective: Building an AI system that overcomes the barriers in enhancer evolution research

To enable cross-species prediction of enhancers, even in cancer-resistant and long-lived animals, we developed EvoPhant, a new AI model built upon DNA language models.

### 3. Results: EvoPhant outperforms existing methods and succeeds in cross-species prediction
① Superior performance on iEnhancer benchmarks

EvoPhant exceeded existing models, with particularly strong performance on EnhancerAtlas (pig, heart).

② Reduced performance on naked mole-rat H3K27ac ChIP-seq data

This dataset defines enhancers using H3K27ac − H3K4me3,
whereas common enhancer definitions often include H3K27ac + H3K4me1.

➡ Differences in labeling criteria may explain the reduced performance, indicating the need for additional experimental validation.

③ Cross-species enhancer prediction using in vivo datasets (LOOSV, human/mouse)

Training on human → predicting mouse: higher performance

Training on mouse → predicting human: lower performance

Analysis of false-positive peaks using ENCODE Screening revealed that
proximal enhancers were frequently enriched, including cCREs not annotated in the original dataset.

➡ EvoPhant appears capable of capturing shared sequence features of proximal enhancers that are conserved across species.

### 4. Future Directions: A foundation for uncovering the mechanisms of cancer resistance and longevity

EvoPhant enables systematic analysis of enhancer evolution in rare species.
By integrating ATAC-seq and other experimental validation, this framework will help elucidate:

How cancer-resistant and long-lived animals evolved their extraordinary phenotypes at the molecular and regulatory levels.
