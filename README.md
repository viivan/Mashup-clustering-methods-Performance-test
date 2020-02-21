# Mashup-clustering-methods-Performance-test
包含T+K、L+K、F+K、F+C+K性能测试代码及相关数据
T+K：该方法先利用TF-IDF技术构建Mashup服务的特征向量，然后利用K-means算法对这些特征向量进行聚类。
L+K：该方法通过LDA模型将Mashup服务描述表示为主题向量的形式。在此基础上，利用K-means算法对主题向量进行聚类。
F+K：该方法利用FSAC方法提取出每条Mashup服务描述（预处理后）的功能名词，并计算它们的功能语义权重。然后，选取功能语义权重较高的单词，结合TF-IDF模型与Word2Vec模型将它们表示成Mashup语义特征向量（简称MFSF向量），直接进行K-means聚类。
F+C+K：该方法也是先将Mashup服务描述表示为MFSF向量，然后通过CCD-DI方法检测出最为合适的K个MFSF向量作为K-means的初始中心，进行聚类。其中，CCD-DI方法中的权重参数a为默认值0.5。
