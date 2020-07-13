# groupby_agg
DataFrame型をgroupbyで集約する時、agg() を使って、平均値や個数のカウントをまとめて行うテクニックを試してみた  

df.groupby('sex').agg(  
    count=('sex', 'count'),     # sex の個数をカウント  
    age_mean=('age', 'mean'),   # age の平均値  
    G1_mean=('G1', 'mean'),     # G1  の平均値  
    G1_median=('G1', 'median'), # G1  の中央値  
    G2_mean=('G2', 'sum'),      # G2  の合計  
    G2_median=('G2', 'max'),    # G2  の最大値  
    G3_mean=('G3', 'min'),      # G3  の最小値  
    G3_median=('G3', 'std')     # G3  の標準偏差  
)  

なお、UCIの学生の成績のデータセットを使っています。  
https://archive.ics.uci.edu/ml/machine-learning-databases/00356/student.zip
