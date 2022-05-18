### 1.国能日新光伏功率预测
+	##### 特征工程      
	> 借位 + 时间，merge 当前气象特征和多久前后的气象特征合并，前面几行(1,2,3)不变    
	> datetime特征   
	> 归一化操作   
	> 匹配month_hour，每个月光照小时数的情况   
	> 每天各个小时段分组，对光照有影响   
	> 同一(年，月，天，小时)在气象各特征的一些统计(最大最小中位数)   
	> 多项式特征 PolynomialFeatures       

### 2.W2V新架子(w2v特征)
	
### 3.补充     
+	##### pandas内置方法     
	> groupby    
	> merge    
	> transform
	> apply    
	> agg(不map)    
	> stats.mode(众数)   
+	##### 知识点补充   
	> lightgbm catboost可以指定类别特征，不需要one-hot category_feature = cate_feature   
		类别特征通过astype("category")设置      
	> onehot对树模型不太必要     
	> get_dummies会自动生成列名，直接onehot不能      
	> target encoder(二分类强特) ctr特征，例如视频点击比赛     
	
	
	
