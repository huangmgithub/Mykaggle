### 1.基于上下文感知的多模态交通推荐服务(导航交通推荐)
+	##### 数据样式
	> 查询记录(train_queries)：    
		查询记录代表百度地图上用户的一条路线搜索。每个查询记录都由会话ID(sid)，配置文件ID(pid)，时间戳(req_time)，    
		原始坐标点位(o)，目的地的坐标组成(d)    
		
	> 显示记录(train_plans):         
		显示记录是百度地图向用户显示的可行路径。每个显示记录由会话ID(sid),时间戳(plan_time)和计划列表(plans)组成    
		每个显示计划包括运输模式，估计的路线距离(以米为单位),估计到达时间(ETA,以秒为单位),估计的价格(RMB),     
		以及间接的显示列表中隐含的显示等级,    
		运输模式可以单模式也可以多模式,    
		运输模式编码到1-11之间的数字标签,    
		例如,[387056,"2018-11-01 15:15:40", [{"mode":1, "distance":3220, "ETA":2134, "price":12},     
		{"mode":3, "distance":3520, "ETA":2841, "price":2}]]是两个运输模式计划的显示记录    

	> 点击记录(train_clicks)：     
		点击记录表示用户对不同建议的反馈，即用户可以点击显示给他/她的某条特定路线以获取详细信息     
		每个记录中，单击数据在显示列表种包含会话ID(sid)，时间戳(click_time)和在显示列表中的点击的     
		传输模式(click_mode)。只保留每个查询的第一点击  

	> 用户属性(profiles):      
		用户配置文件属性反映了用户对传输模式的个人偏好。每个会话的用户通过配置文件ID(pid)与一组用户属性关联(p0-p65)    
		每个配置文件记录由一个配置文件ID,一组热编码的用户配置文件维度组成   
		相同属性的用户与相同的用户配置文件ID合并，例如考虑到性别和年龄，数据集将两个35岁的男性标识为相同的用户   
+	##### 数据分析和处理    
	> EDA数据基本信息    
	> EDA变量相关性分析    
	> 构建baseline    
+	##### 可提升    
	> od -> w2v  强特o和d结合    
	> 增加stacking和伪标签    
	> CounterVectorizer & w2v: 例如处理plans，o和d， w2v后，累加，平均一下，类似句子embedding    
