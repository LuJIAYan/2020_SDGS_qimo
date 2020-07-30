# 2020SDGS_qimo 期末项目

项目名称 | 中国特色联合国发展：联合国发展目标与习近平新时代中国特色社会主义思想之主题模型可视化
---|---
小组成员 | 卢佳燕 周昱瑾 孙思盼



* 主故事板来源(30%完成): 
* 习近平新时代中国特色社会主义思想 文本 (85%完成, mining)
* 联合国发展目标 文本 (100%完成, mining)
* 数据(85%完成): 上述两文本源(中文来源)
* 代码(50%完成): 要调整改Pandas及Mining的代码, 会应用LDA主题模型



# 一、主故事板来源
我们的项目是针对合国发展目标与习近平新时代中国特色社会主义思想的文本分析项目。我们计划以联合国17个发展目标和习近平新时代中国特色社会主义思想展开探讨。

通过web数据挖掘爬取习近平新时代中国特色社会主义思想三十讲、习近平新时代中国特色社会主义思想学习纲要（19个）、生态文明建设相关的文章的文本内容进行LDA主题模型应用，最终产出相应的可视化产品，挖掘习近平新时代中国特色社会主义思想实践探索与联合国17个可持续发展目标有没有异同点，挖掘习近平新时代中国特色社会主义思想实践探索的特点，促进其可持续发展。

![image](https://github.com/LuJIAYan/2020_SDGS_qimo/blob/master/images/数据流程与猜想.png)

### 1.1背景
- 联合国发展目标：

    联合国所有会员国于2015年通过的《 2030年可持续发展议程》为当今和未来的人类与地球的和平与繁荣提供了共同的蓝图。它的核心是17个可持续发展目标（SDG），这是所有国家（无论是发达国家还是发展中国家）在全球伙伴关系中迫切需要采取的行动。他们认识到，消除贫困和其他贫困现象必须与改善健康和教育，减少不平等并刺激经济增长的战略紧密结合，同时应对气候变化并努力保护我们的海洋和森林。
    
![image](https://github.com/LuJIAYan/2020_SDGS_qimo/blob/master/images/17goal.jpg)

- 习近平新时代中国特色社会主义思想：

    习近平新时代中国特色社会主义思想，从理论和实践结合上系统回答了新时代坚持和发展什么样的中国特色社会主义、怎样坚持和发展中国特色社会主义这一重大时代课题，是马克思主义中国化最新成果，是当代中国马克思主义、21世纪马克思主义，是党和国家必须长期坚持的指导思想。深入学习贯彻习近平新时代中国特色社会主义思想，必须深刻认识领会这一思想的时代意义、理论意义、实践意义、世界意义。习近平新时代中国特色社会主义思想顺应和平、发展、合作、共赢的时代潮流，推动构建新型国际关系和人类命运共同体，为世界和平与发展作出重大贡献。
    

![image](https://github.com/LuJIAYan/2020_SDGS_qimo/blob/master/images/China.jpg)

### 1.2相关文本内容来源：
- 一、[联合国17个发展目标](https://sustainabledevelopment.un.org/partnerships/goodpractices)

- 二、[习近平新时代中国特色社会主义思想三十讲](http://www.qstheory.cn/xjpsxkj/index.html)

- 三、[习近平新时代中国特色社会主义思想学习纲要（19个）](http://theory.people.com.cn/GB/68294/428935/)

- 四、[生态文明建设](http://theory.people.com.cn/GB/68294/417224/index.html)

- 五、习近平广东等其他重要讲话

### 1.3中国故事：
预测：
* 共性：习近平新时代中国特色社会主义思想实践偏向良好健康福祉（goal 3）、优质教育（goal5）、体面工作和经济增长（goal8）、产业创新和基础设施（goal9 ）、减少不平等（goal10）
* 个性：符合人民日益增长的文化需求、具有中国社会主义特色、科学发展观

# 二、代码
### 2.1 [web mining](https://github.com/LuJIAYan/2020webmining/tree/master/SDGS_qimo)
* [生态文明、习近平新时代中国特色社会主义思想三十讲](https://github.com/LuJIAYan/2020_SDGS_qimo/blob/master/web_mining/%E7%94%9F%E6%80%81%E6%96%87%E6%98%8E%E7%88%AC%E8%99%AB/getContents.ipynb)
* [联合国17个发展目标、习近平新时代中国特色社会主义思想学习纲要（19个）](https://github.com/LuJIAYan/2020_SDGS_qimo/blob/master/web_mining/get_content%E4%BB%A3%E7%A0%81%E9%9B%86.ipynb)
### 2.2 LDA主题模型应用
* [数据清理、断词](https://github.com/LuJIAYan/2020_SDGS_qimo/blob/master/LDA/LDA_0629/SDG_%E6%95%B0%E6%8D%AE%E6%B8%85%E7%90%86_01_%E6%95%B0%E6%8D%AE%E6%B8%85%E7%90%86_%E8%BF%AD%E4%BB%A301.ipynb)
* [半监督修正](https://github.com/LuJIAYan/2020_SDGS_qimo/blob/master/LDA/LDA_0629/data_sets/raw_data_SDG_processed.xlsx)
* LDA_01_主题建模_主题模型批量产出
* LDA_02A_主题建模_pyLDA交互可視化批量产出
* LDA_02B_主题建模_热点图交互可視化批量产出
