# Azure认知搜索方案

因为Azure认知搜索技术成熟，而且相对功能也比较多，对于一些复杂的场景推荐使用。

<img width="1121" alt="Screen Shot 2023-06-08 at 11 18 19 AM" src="https://github.com/huqianghui/pdf-form-table-demo-test-script/assets/7360524/510a093b-8289-4ef4-9abb-930a8f510a09">

1. 索引创建

   1）索引分类

   2）一些其他的设置：容量和副本等 

   3） 解析器选择 --中文处理


2. 非结构化文档索引化
   
  1)  PDF 文件读取处理： 表单识别
      
      内容处理：
      
      1）表格内容table;  
      
      2）checkbox 选中项; 
      
      3）图片（透视图等） 
   
  2) 长文件切割 
     
     a） chrunk大小;
      
     b） overlap大小;
     
     c） 断句以及追溯段大小
  
  <img width="296" alt="Screen Shot 2023-06-08 at 11 20 54 AM" src="https://github.com/huqianghui/pdf-form-table-demo-test-script/assets/7360524/3b61e068-d745-4ddd-b96c-dd0007c50138">
       
3. 调用过程
    
      1）搜索语法 --中文处理;
      
      2) 阈值score确定;
     
      3) 使用语义搜索;
      
      4) prompt设置，让它更精准;
      
      5) 模型选择： davince, chatgpt，gpt4，gpt4-32K;
      
      6) 模型参数设置;
  
  <img width="397" alt="Screen Shot 2023-06-08 at 11 21 01 AM" src="https://github.com/huqianghui/pdf-form-table-demo-test-script/assets/7360524/75dc0212-fce2-42a9-b47a-f502858e6f60">
    
 4. framework 选择
     
     1） langchain： 解决重试，缓存，数据获取等
     <img width="1058" alt="Screen Shot 2023-06-08 at 11 16 26 AM" src="https://github.com/huqianghui/pdf-form-table-demo-test-script/assets/7360524/81c9fda1-a20f-4a94-a016-9337422cedbf">

     2） Senamic Kernel

    <img width="1044" alt="Screen Shot 2023-06-08 at 11 17 17 AM" src="https://github.com/huqianghui/pdf-form-table-demo-test-script/assets/7360524/8a9b2b52-ab5e-4ace-9115-d060c03e6712">





