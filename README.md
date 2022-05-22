# Baseline-LabelSimilarity

## 説明
各カテゴリの特徴量と文章のn-gram（1,2,3）に対してコサイン類似度を計算。
コサイン類似度が最大のカテゴリへ分類。

## 学習済みWord2Vecモデル
Googleニュースデータセットの一部（約1,000億語）でトレーニングされた事前学習済みモデル。モデルには、300万の単語とフレーズの300次元のベクトルが含まれる。  
https://github.com/mmihaltz/word2vec-GoogleNews-vectors
から`GoogleNews-vectors-negative300.bin`をダウンロード

## テストデータ
### DBpediaデータセット
DBpedia2014から14クラスを選択したもの。クラス情報は単語間にスペースを挿入。学習データは、各40,000、計560,000、テストデータは、各5,000、計70,000。
https://drive.google.com/uc?export=download&id=0Bz8a_Dbh9QhbQ2Vic1kxMmZZQ1k
から取得。
- dbpedia_csv
    - class.txt
    - readme.txt
    - train.csv
    - test.csv

## 前処理
- 括弧内文章の削除
- 記号文字の削除
- 著者名の削除
- スペースの調整