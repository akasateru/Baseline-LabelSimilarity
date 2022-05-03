Baseline-LabelSimilarity

説明：
    各カテゴリの特徴量と文章のn-gram（1,2,3）に対してコサイン類似度を計算。
    クラス名から取得したベクトルと文書に出現する全ての n-gram(n=1,2,3) に対してコサイン類似度を計算。
    最上位の類似度が閾値を上回るとき，そのクラスに割り当てる。

学習済みWord2Vecモデル：
    Googleニュースデータセットの一部（約1,000億語）でトレーニングされた事前学習済みモデル。
    モデルには、300万の単語とフレーズの300次元のベクトルが含まれる。
    https://code.google.com/archive/p/word2vec/

    GoogleNews-vectors-negative300.bin
    from https://github.com/mmihaltz/word2vec-GoogleNews-vectors

テストデータ：
    DBpediaデータセット
    DBpedia2014から14クラスを選択したもの。

    dbpedia_csv
        class.txt   14クラス。単語間にスペースを挿入。
        readme.txt
        test.csv    各40,000　計70,000
        train.csv   各5,000　計560,000
    from https://drive.google.com/uc?export=download&id=0Bz8a_Dbh9QhbQ2Vic1kxMmZZQ1k
    
前処理：
    括弧内文章の削除
    記号文字の削除
    著者名の削除
    スペースの調整

クラスのベクトル：
    文章中の単語の特徴量の和を単語数で割る

閾値：
    なし