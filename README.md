Baseline-LabelSimilarity

説明：
    文章と各カテゴリの特徴量を比較し、類似度が最も高いカテゴリへ分類。
    単語の特徴量は、Word2Vecを用いて計算し、文章の特徴量は、単語の特徴量の和を単語数で割ったものとする。

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

文章のベクトル：
    文章中の単語の特徴量の和を単語数で割る



