# Embeddings Solution

Embeddings是一种特殊的数据表示形式，可以对一段文本的语义含义进行信息密集表示。每个Embeddings都是浮点数类型的向量。

在向量空间中两个Embeddings的距离与原始格式的两个输入文本之间的语义相似性相关。换句话说，如果两个文本相似，则它们的向量表示也应相似。因此，Embeddings 使得语义空间的搜索匹配成为可能。

一种典型的基于Embeddings的企业私域数据 Q&A 方案架构： 

![image](https://github.com/ZEGUK/pdf-form-table-demo-test-script/assets/32155786/a606bd28-3e29-4943-aace-12811e5290e3)

1） Embeddings 向量生成

如果熟悉机器学习与深度学习，那么对Embeddings一定不陌生。机器学习的内核即为对数据进行高维度的抽象表达，从而更精细地了解数据特征（Feature)。数据的高维度抽象表达会生成特征向量，一个数据的所有特征向量构成向量空间。

其中，高维度的抽象表达如果是通过深度学习模型中的专有层（layer)对原始数据进行空间映射来实现，这种抽象表达就是Embeddings；如果通过简单的机器学习模型进行空间映射，得到的抽象表达就是数据特征。因此，数据特征可以理解为广义的Embeddings。

能够生成Embeddings 的模型/算法也不仅仅只有GPT，实际上几乎所有的深度学习模型都可以生成广义的Embeddings, 只不过在自然语言处理领域，特别是大语言模型方向，Embeddings因为GPT的强大而逐渐被大家关注。

在上图中，使用text-embeddings-ada-002作为Embeddings的生成模型。


2） Embeddings 存储选择

Embeddings的存储涉及到向量存储与检索。在Azure平台上，支持向量存储和检索的有：PostgreSQL  和 Redis Enterprise。在开源社区，向量数据库例如：Qdrant、Pinecone、Redis、Weaviate、Milvus...

关于开源向量数据库的性能测评，可以参考：

https://jina.ai/news/benchmark-vector-search-databases-with-one-million-data/


3） Embeddings 向量相似性搜索中的阈值设置
