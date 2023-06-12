# Private Domain Knowledge Base(KB) Process

随着openAI和chatGPT的火爆，大家都想把这个利器转化为生产力，让自己事半功倍。 

大家最先能想到的使用场景，就是利用它实现企业内部知识问答。原因如下：

1） 作为一个试验田，先企业内部使用，不涉及到C端客户，对安全和性能的要求没那么高。

2） 可以有效规避一些个人数据出境等风险。

3） 很多企业内部都有大量文档和一个不经常使用到的 Q&A Bot，大家都对它早就失去了耐心和兴趣，所以很多时候还是走人工流程、电话和邮件之类的方式。所以大家想到，只要简单替换API应该就有质的飞跃。

说干就干就是我中国互联网和IT人员的作风，于是开始准备申请立项。考虑到GPT模型的知识库停留在2021年9月，后面即使有多次迭代更新，知识库并没有变。

面对这种情况的第一个选择是：是否可以通过fine-tune，把企业的知识库和少量的公域知识库通过fine-tune的方式喂给GPT模型，让其“知识储备”满足企业要求呢？

在做fine-tine之前，需要了解以下几个情况：

1）目前默认只提供Ada、Babbage和Curie三类模型的调优，Davinci类模型需要额外申请。 也就是fine-tune模型没有办法利用GPT-3/3.5(ChatGPT所用模型）和最新GPT-4的更加强大的能力。 

2）因为企业内部知识也在变更，意味着训练也不是一锤子买卖，需要不停的迭代。 

3）GPU资源很贵很紧张，大家看英伟达的股价就知道了。  

因此，第一种方式通常不是利用GPT实现企业内部知识问答的最佳选择。

第二种选择即：通过提示词工程 + 建立索引的方式将企业的知识库“外挂”到GPT模型。目前开源社区给出了两个方案，得到了大家的广泛使用。

1） 基于Azure Cognitive Search实现数据索引  

![appcomponents](https://github.com/huqianghui/pdf-form-table-demo-test-script/assets/7360524/c790842a-c4cb-4ffd-8615-ec9916c40667)

2） 通过Vector Embedding，实现数据的向量化并进行向量相似性搜索 

<img width="985" alt="Screen Shot 2023-06-08 at 10 48 43 AM" src="https://github.com/huqianghui/pdf-form-table-demo-test-script/assets/7360524/84a7efa7-1d81-4b6d-a035-e6a2cc7475a5">



它们都是在解决私域数据如果被正确地吐给GPT模型，GPT模型可以给出一个正确的私域答案。但是基于上面两个链接，大家在使用之后发现效果差强人意。通过一些实践，这里整理了一些关键点供大家参考。
