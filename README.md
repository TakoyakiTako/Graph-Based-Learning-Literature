# ICML Graph Based Learning

### ICMLのGraphLearningの論文集めました

## ・Simplifying Graph Convolutional Networks
<details><summary>概要</summary>
GCNは最近のDeepLearningアプローチからひらめきを得ている  
結果として、不必要な複雑性と計算量を引き継いでしまった  

##### 提案
SGCを提案  
継続的な非線形性を除き、連続した層の間の重み行列の崩壊を通して、上記のような過剰な複雑性を減らす  
理論的に結果として生じる線形モデルを分析し、固定されたlowpassfilterに一致する  

##### 実験
単純化が精度に対して負の影響を与えないことを示した  
さらに大きいデータセットに対して自然な解釈が可能となり、FastGCNより2桁分ぶんスピードアップした  
</details>

## ・Disentangled Graph Convolutional Networks

<details><summary>概要</summary>
既存のGraphデータに対するDLメソッドは潜在的な要素のもつれを無視している   
しかし潜在的な要素のもつれを解いた表現を学習することは非常に難しいし、GNNの研究で未開のままである  

##### 提案  
DisenGCN（disentangled graph convolutional network）という新しいGNNを提案  
もつれを解いたノード表現を学習する  
特に微分可能で帰納的学習と形式でそれぞれのエッジの構造の背後にあるfactorを参照するための新しい隣接ルーティングメカニズムを提案  
また理論的にroutingメカニズムの集合の性質を証明、そして実験的にもつれを解いた表現の学習の利点を示した。  

##### 実験
・Citeseer, Cora, and Pubmed for semi-supervised node  
・BlogCatalog, PPI, POS  for multi-label node classification  

#### future work  
もつれを解いたノード表現が、より包括的なGraphを表現するようなGraph全体に対して単一の表現を導くために利用されうるかどうかを調査する  
</details>

## ・Position-aware Graph Neural Networks

<details><summary>概要</summary>
・広範囲なgraph構造の中のnodeの位置をとらえたnode埋め込みを学習することはgraph上の多くの予測タスクで重要  
・既存のGNNのアーキテクチャはノードのposition/locationなどをとらえる能力が制限されている  

##### 提案  
・Position-aware Graph Neural Networks (PGNNs)を提案  
・Nodeのpositionを意識したノード埋め込みを計算する  
・アンカーノードのセットをsampling  
→それぞれのアンカーセットNodeとtaegetnodeとの距離を計算する  
→安価セット全体にわたり非線形距離重みを持つaggregation schemeを学習  

・P-GNNsの利点  
  ・帰納的  
  ・拡張可能  
  ・ノードの特徴情報を集める  

##### 実験  
・link prediction task	: Grid、Communities、PPI  
・community detection	: Communities、Emails、Protein  
</details>

## ・GMNN: Graph Markov Neural Networks
<details><summary>概要</summary>

relational dataによるsemi-supervisedなobject classificationの研究  

以下の両方で広範囲で研究されているrelational relational dataにおける基本的な問題に取り組む  
statistical relational learning (例 relational Markov networks)  
graph neural networks (例 graph convolutional networks)  

統計的関係モデルはCRFを通して効率よくオブジェクトラベルの関係をモデル化できる  
GNNはend-to-endな学習を通して効率的にオブジェクト表現を学習できる  


#### 提案
Graph Markov Neural Network (GMNN)  

統計的関係モデルとGNNの両方の利点を組み合わせた  
EMアルゴリズムによって効率的に学習し、CRFを持つオブジェクトラベルの同時分布をモデル化  
E-step  
GNNによりオブジェクトラベルの事後分布を予測するために効果的なオブジェクト表現を学習  
M-step  
別のGNNが局所的なラベルの依存関係をモデル化する  

#### 実験
object classification：Cora, Citeseer, Pubmed（SOTA）  
link classification：Cora, Citeseer, Pubmed  
unsupervised node representation learning：Bitcoin, Alphahe Bitcoin OTC（SOTA）  
</details>

## ・DAG-GNN: DAG Structure Learning with Graph Neural Networks
<details><summary>概要</summary>

接続の分布のサンプルから正確な有向非巡回Graph（DAG、たどっても自分のノードには戻らないGraph）を学習することは難しい  
それはGraphのノードの数において指数関数以上の探索空間があるためである（NP困難）  

#### 提案  
複雑な非線形マッピングをとらえる能力があるDLをモチベーションとして  
deep generative modelを提案し、様々な構成上の制約に対してDAGを学習させる  

Generative modelの中心で新しいGNNに基づいたvariational au-toencoder（DAG-GNN）を提案  
モデルの豊富なcapacityに加えて、ベクトル値の変数に加えて離散変数も自然に取り扱える  
GNNを使用することでパラメトリックモデルによって生成されたデータだけでなく、スカラー/ベクトルや連続/非連続などのデータにも対処することができる  

#### 実験  
dataset：Child, Alarm, Pigs, 線形と非線形のSEMsから生成された合成データ  

</details>

## ・Learning Discrete Structures for Graph Neural Networks
<details><summary>概要</summary>
</details>

## ・Self-Attention Graph Pooling
<details><summary>概要</summary>
</details>

## ・Graph U-Net
<details><summary>概要</summary>
</details>

## ・Deep Relational Pooling
<details><summary>概要</summary>
</details>

## ・Distributed, Egocentric Representations of Graphs for Detecting Critical Structures
<details><summary>概要</summary>
</details>

## ・Graph Element Networks: adaptive, structured computation and memory
<details><summary>概要</summary>
</details>

## ・LatentGNN: Learning Efficient Non-local Relations for Visual Recognition
<details><summary>概要</summary>
</details>

## ・Graph Matching Networks for Learning the Similarity of Graph Structured Objects
<details><summary>概要</summary>
</details>

## ・Stochastic Blockmodels meet Graph Neural Networks
<details><summary>概要</summary>
</details>

## ・Adversarial Attacks on Node Embeddings via Graph Poisoning
<details><summary>概要</summary>
</details>

## ・MixHop: Higher-Order Graph Convolution Architectures via Sparsified Neighborhood Mixing
<details><summary>概要</summary>
</details>

## ・Open Vocabulary Learning on Source Code with a Graph-Structured Cache
<details><summary>概要</summary>
</details>

## ・Graphite: Iterative Deep Generative Modeling of Large Graphs
<details><summary>概要</summary>
</details>

## ・Functional Transparency for Structured Data: a Game-Theoretic Approach
<details><summary>概要</summary>
</details>

## ・Graph Convolutional Gaussian Processes
<details><summary>概要</summary>
</details>

## ・Geometry Aware Convolutional Filters for Omnidirectional Images Representation
<details><summary>概要</summary>
</details>

## ・Geometric Scattering for Graph Data Analysis
<details><summary>概要</summary>
</details>

## ・GEOMetrics: Exploiting Geometric Structure for Graph-Encoded Objects
<details><summary>概要</summary>
</details>

## ・Circuit-GNN: Graph Neural Networks for Distributed Circuit Design
<details><summary>概要</summary>
</details>

## ・Graph Neural Network for Music Score Data and Modeling Expressive Piano Performance
<details><summary>概要</summary>
</details>
