### 1.面向电信行业存量用户的智能套餐个性化匹配模型
+   #### EDA
	> 复赛数据集中套餐999999只有2个，且初赛数据集无套餐999999, 少量数据可能对平均f1_score影响很大, 可删除
	> 初赛数据集service_type中没有套餐3，复赛数据集中存在少量套餐3, 将套餐3改为套餐4
+   #### W2V对4个月的金额做特征(10个额外特征)
+   #### 对复赛数据(训练集和测试集)预测，进行Stacking
+   #### 特征工程      
	> ##### 原始特征    
		origin_cate_feature和origin_num_feature      
	> ##### 统计特征     
		函数feature_count     
		话费，流量，上网时间等进行计数统计     
		话费，流量，上网时间等分别和套餐类型和合约类型交叉统计特征    
		其他: 当月话费占比，各同类型流量话费比例等    
	> ##### 差值特征    
		对应diff_feature_list 1-4月费用相邻之间的差值    
		其他同类别计数特征之间的差值，例如流量，通话时长    
	> ##### w2v特征   
		对应函数w2v_feature   
	> ##### stacking特征    
		对应函数stacking_feature   
+   #### 相关链接
		比赛 https://www.datafountain.cn/competitions/311/datasets
		项目 https://github.com/PandasCute/2018-CCF-BDCI-China-Unicom-Research-Institute-top2
		嫁接 https://github.com/plantsgo/ijcai-2018
	   
### 2.补充
+	loc和iloc用法补充
+   读取文件
	> csv库读取文件
    > chunksize 针对大数据集，分批读取数据

