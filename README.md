# B3 Project 2026

2026年度B3研究プロジェクト用の講義・演習資料です。ニューラルネットワークの量子化、モデル圧縮、Looped LLMの計算特性を、実装と実験を通して評価します。

## 基礎講義

- [第1回：ニューラルネットワークと量子化の基礎](docs/class_01.ipynb)
- [第2回：モデル圧縮と評価方法](docs/class_02.ipynb)

## 演習テーマ

| テーマ | 内容 | Notebook |
|---|---|---|
| A | 重みとアクティベーションの量子化感度評価と、効率的な量子化パラメータ設定方法の検討 | [GitHub](theme_A/theme_A.ipynb) / [Colab](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_A/theme_A.ipynb) |
| B | ニューラルネットワークの重みにおけるベクトル量子化とスカラー量子化の効率比較、および融合手法の検討 | [GitHub](theme_B/theme_B.ipynb) / [Colab](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_B/theme_B.ipynb) |
| C | 量子化の前処理としてのアダマール変換の効果 | [GitHub](theme_C/theme_C.ipynb) / [Colab](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_C/theme_C.ipynb) |
| D | 量子化と多層分解を同時に行う場合の、深さとビット幅の最適比 | [GitHub](theme_D/theme_D.ipynb) / [Colab](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_D/theme_D.ipynb) |
| E | 量子化と枝刈りを同時に行う場合の、ビット幅とスパーシティの最適比 | [GitHub](theme_E/theme_E.ipynb) / [Colab](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_E/theme_E.ipynb) |
| F | Looped LLMにおける重み量子化ビット幅と、精度・モデルサイズのトレードオフ | [GitHub](theme_F/theme_F.ipynb) / [Colab](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_F/theme_F.ipynb) |
| G | Looped LLMの再帰回数と、精度・収束性・計算量の関係 | [GitHub](theme_G/theme_G.ipynb) / [Colab](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_G/theme_G.ipynb) |

## 演習の進め方

1. 担当テーマのNotebookをGoogle Colabで開く。
2. Notebook冒頭の指示に従ってランタイムと必要なライブラリを準備する。
3. 研究上の問いと、実験前の予想を記録する。
4. 基準条件の結果を確認してから、独立変数を変更する。
5. 他の条件は可能な限り固定し、結果を表とグラフで比較する。
6. Notebook末尾の課題に加えて、少なくとも1つの追加実験を行う。

Notebookのデフォルト設定は動作確認を目的としています。最終結果を作成するときは評価データ量や試行条件を増やし、同じ傾向が得られるか確認してください。

## 発表・提出内容

発表資料には、少なくとも以下を含めてください。

1. 研究上の問いと実験前の予想
2. 独立変数・統制変数・評価指標
3. 基準条件と各実験条件の結果
4. 表およびグラフによる比較
5. 追加実験
6. 結果に対する考察と結論
7. 実験の限界と、次に調べるべき点

最良の結果だけでなく、性能が低下した条件や予想と異なった結果も報告してください。
