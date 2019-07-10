# ICML Graph Based Learning


<details><summary> ## ・Simplifying Graph Convolutional Networks </summary>
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

future work  
もつれを解いたノード表現が、より包括的なGraphを表現するようなGraph全体に対して単一の表現を導くために利用されうるかどうかを調査する  

## ・Position-aware Graph Neural Networks

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

## ・GMNN: Graph Markov Neural Networks

## ・DAG-GNN: DAG Structure Learning with Graph Neural Networks

- どんな論文
