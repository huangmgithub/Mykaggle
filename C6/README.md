### 1.模型融合
+   分类stacking
    >  from mlxtend.classifier import StackingClassifier
### 2.房价预测
+   增加特征重要性feature_importance   
	> 5-kfold相加得到的特征重要性    
	> 筛选出特征重要性为0的特征，删除特征


### 2.Recruit Restaurant Visitor Forecasting
+ ##### https://www.kaggle.com/code/headsortails/be-my-guest-recruit-restaurant-eda/report # EDA
+ ##### https://www.kaggle.com/code/zeemeen/weighted-mean-comparisons-lb-0-497-1st/script  # weighted mean   
+  baseline 特征工程
   * hr内连接id关联到air_store_id
   * 列出tes不重复的air_store_id->stores
   * stores关联tra新特征(air_store_id, dow)
   * stores关联as(air_store_id)
   * tra&tes关联hol(visit_date)   
+  weighted mean  
+  时间序列      
### 3.房价预测  
+  lgb xgb ctb lr训练
+  stacking模型融合