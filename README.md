# B3 Project 2026

2026年度B3研究プロジェクト用の講義・演習資料です。ニューラルネットワークの量子化、モデル圧縮、Looped LLMの計算特性を、実装と実験を通して評価します。

## 基礎講義

- [第1回：ニューラルネットワークと量子化の基礎](docs/class_01.ipynb)
- [第2回：モデル圧縮と評価方法](docs/class_02.ipynb)

## 演習テーマ

- [テーマA](theme_A/theme_A.ipynb)：重みとアクティベーションの量子化感度評価と、効率的な量子化パラメータ設定方法の検討
- [テーマB](theme_B/theme_B.ipynb)：ニューラルネットワークの重みにおけるベクトル量子化とスカラー量子化の効率比較、および融合手法の検討
- [テーマC](theme_C/theme_C.ipynb)：量子化の前処理としてのアダマール変換の効果
- [テーマD](theme_D/theme_D.ipynb)：量子化と多層分解を同時に行う場合の、深さとビット幅の最適比
- [テーマE](theme_E/theme_E.ipynb)：量子化と枝刈りを同時に行う場合の、ビット幅とスパーシティの最適比
- [テーマF](theme_F/theme_F.ipynb)：Looped LLMにおける重み量子化ビット幅と、精度・モデルサイズのトレードオフ
- [テーマG](theme_G/theme_G.ipynb)：Looped LLMの再帰回数と、精度・収束性・計算量の関係

## テーマF・Gについて

テーマF・Gでは、Looped LLMの [ByteDance/Ouro-1.4B](https://huggingface.co/ByteDance/Ouro-1.4B) を使用します。

| テーマ | 変更する条件 | 固定する条件 | 主な評価項目 |
|---|---|---|---|
| F | 重みビット幅（16/8/6/4/3/2-bit） | 再帰回数4回 | Perplexity、next-token accuracy、理論モデルサイズ、生成文 |
| G | 再帰回数（1〜8回） | 16-bit重み | Perplexity、next-token accuracy、JS divergence、hidden state変化、生成文 |

テーマFでは量子化ビット幅だけを、テーマGでは再帰回数だけを独立変数として扱います。複数の条件を同時に変えず、結果の原因を区別できる実験計画にしてください。

### Colabで開く

- [テーマFをGoogle Colabで開く](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_F/theme_F.ipynb)
- [テーマGをGoogle Colabで開く](https://colab.research.google.com/github/ArtIC-TITECH/b3-proj-2026/blob/main/theme_G/theme_G.ipynb)

### 実行環境

- Google Colab
- GPU：T4
- モデル：Ouro-1.4B
- データセット：WikiText-2

Notebookを開いたら、「ランタイム」→「ランタイムのタイプを変更」から **T4 GPU** を選択してください。最初の環境セットアップでパッケージが更新された場合だけ、セッションを一度再起動し、その後Notebookを先頭から実行します。

デフォルトの評価系列数は動作確認用に小さく設定されています。最終結果を作成するときは評価系列数を増やし、同じ傾向が得られるか確認してください。

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

