# 第三周作业
### 本次作业主要分为四块内容：
### 一、可视化工具整理
### 二、数据集
### 三、对数据集的可视化呈现
### 四、使用体会
## 

## 一、国内外免费图表制作工具整理
### 在线
- **RAWGraphs** [https://rawgraphs.io/](https://rawgraphs.io/)
  
  ![Rawgraphs页面](https://github.com/ChenM-7/CM-task/blob/master/week3/02%20Rawgraphs.png)

  图表类型很丰富，除了常见的柱状图、散点图外，还包括其他一些很神奇的图表（如下图）
  
  除了可以生成常规的png格式图片，还可以生成SVG代码（！），便于直接复制到网页代码中呈现可视化效果。
  
  ![Rawgraphs图表](https://github.com/ChenM-7/CM-task/blob/master/week3/01%20Rawgraphs.png)
  
  
- **ChartBlocks** [https://www.chartblocks.com/en/](https://www.chartblocks.com/en/)
  
  ![Chartblocks页面](https://github.com/ChenM-7/CM-task/blob/master/week3/03%20Chartblocks.png)
  
  
- **Datawrapper** [https://www.datawrapper.de/](https://www.datawrapper.de/)

  除了图表还可以制作交互式地图！无法免费下载，但可以用网页形式分析。
  
  ![Datawrapper页面](https://github.com/ChenM-7/CM-task/blob/master/week3/04%20Datawrapper.png)
  
  
  
- **Infogram** [https://infogram.com/](https://infogram.com/)
  
  除了可以制作图表外，还有多种信息图表排版可供选择！（忍不住感慨：太方便了吧！）
  
  无法免费下载，但可以以网页形式分享，保持了交互的特性！
  
  ![infogram页面](https://github.com/ChenM-7/CM-task/blob/master/week3/05%20infogram.png)
    
 
### 软件
- **Tableau**
  
  可以免费申请学生版，操作（自我感觉）比前面的在线工具更加复杂，但功能也更强大。
  
- **Python**

  这就得靠码代码了，可以利用如pandas和matplotlib等库进行可视化制作。

- **D3.js**

   一个资源丰富的开源的JavaScript函数库，从上一届师哥师姐了解到，他们的很多作品可视化的实现都少不了D3.js。（估计这也是我未来要啃的一个大头）

- **Echartshttps**[www.echartsjs.com/zh/index.html](www.echartsjs.com/zh/index.html)

  也是一个纯javascript的数据可视化库。
 
- **Excel**

  Excel虽然看起来很朴素（？），但也是一款很实在的图表制作软件！（大一不会做好看的数据图，那时候写社会调查报告时用的图表就都来自Excel hhhh)
  
- **Adobe系列：AI+PS、AE**

  AI、PS可以直接用来做图表，也可以把从其可视化工具（如tableau）中做出来的图表拖进去进一步完善。
  
  AE则能实现动态图表的制作。
  
  
## 二、数据集
  
  ![数据集](https://github.com/ChenM-7/CM-task/blob/master/week3/06%20suicide%20rates.png)

**1985年至2016年自杀率概述——按年份和国家比较社会经济信息和自杀率**

这是我从kaggle中选取的数据集，选择时主要考虑了以下几点：

1. **内容**：
  
  如下图，这个自杀数据集除了包括国家、自杀人数之外，还进行了性别、年龄的进一步划分，此外还试图将自杀数据和社会经济发展情况相结合，这个切入点很有意思。“自杀”这一社会行为背后映射出的不仅仅是个人性格和际遇，还有整个社会环境的变化。
  
  ![数据集-列](https://github.com/ChenM-7/CM-task/blob/master/week3/10%20%E6%95%B0%E6%8D%AE%E9%9B%86-%E5%88%97.png)
  
  这是对数据集内容的描述和数据来源（参考文献）：
  
  ![数据集内容](https://github.com/ChenM-7/CM-task/blob/master/week3/09%20%E6%95%B0%E6%8D%AE%E9%9B%86%E6%8F%8F%E8%BF%B0.png)

2. **usability（易用性/可用程度）**：

  kaggle对usability的描述如下，符合越多项，可用程度越高。
  
<p align="center">
	<img src="https://github.com/ChenM-7/CM-task/blob/master/week3/08%20%E6%98%93%E7%94%A8%E6%80%A71.png" alt="Sample"  width="300" height="500">
	<p align="center">
		<em> 数据的集易用性 </em>
	</p>
</p>
  

  本数据集的易用性为7.1，在kaggle中大概处于中等偏上的位置，虽然没有达到最高（10.0），但一方面我觉得用来做本次的数据呈现已经足够，另一方面我个人对这一话题的也很感兴趣hhh，两相结合最终选择了这个“自杀数据集”。
  
## 三、可视化呈现

### 过程
#### （一）
首先下载数据集，在Excel里顺利打开，一共有27820条数据，变量包括国家、年份、性别、年龄、自杀人数、该年龄和性别对应的总人口、国家全年GDP和人均GDP等。
  
![excel1](https://github.com/ChenM-7/CM-task/blob/master/week3/11%20excel1.png)

#### （二）datawrapper-世界地图
粗略浏览了一下，我发现这一数据集包括了81个国家，同时并不是每个国家都有完整的从1985-2016所有年份的自杀数据，比较了一下之后我选择了2012年的数据，这一年的数据相对全面。在excel中筛选出各国2012年的数据，分别用求和公式（SUM）算出自杀的总人数（整个过程大概花了三十分钟,可能是本小白还不太熟练excel吧/捂脸）。

把数据填进**datawrapper**，前面有说，这个在线工具可以直接做可视化地图！虽然不能直接免费下载，但可以生成可交互的网页链接（可视化小白表示非常惊喜⊙▽⊙）！

链接：[2012年世界自杀人数统计（部分国家）](https://www.datawrapper.de/_/TIM5U/)

效果如下（截图）：

![图表1](https://github.com/ChenM-7/CM-task/blob/master/week3/%E5%9B%BE%E8%A1%A81-%E5%9C%B0%E5%9B%BE.png)

#### （三）datawrapper-折线图

那么单个国家的自杀情况如何呢？本来想以美国为例进行说明，但发现自杀人数基数太大了，用图表呈现很难体现出差别和变化，于是转而找了一个小国家——亚美尼亚（Armenia）。具体情况如下：

继续用**datawrapper**——在Excel中计算出1990-2016男性和女性自杀人数，这次用图表来呈现：

链接：[1990-2016年亚美尼亚男女性自杀人数统计](https://www.datawrapper.de/_/OCRly/)（有交互效果）

效果如下（截图）：

![图表2](https://github.com/ChenM-7/CM-task/blob/master/week3/%E5%9B%BE%E8%A1%A82-%E6%80%A7%E5%88%AB%E3%80%81%E6%8A%98%E7%BA%BFdatawrapper.png)

#### （四）Infogram-折线图+信息图表

  继续探索，我又发现了一个神奇的在线可视化工具——**Infogram**！不仅可以做各种图表，还有各种排版模板（排版小白的生命之光）！

  正好在里面发现了一个适合“性别”的图表排版，于是继续用前面的数据。

  链接：[1990-2016年亚美尼亚男女性自杀人数统计](https://infogram.com/yellow-negative-1hnq41mr5rzk43z?live)（一定要点开鸭！不然看不到交互效果qwq）

  效果如下（截图）：
  
  ![图表3](https://github.com/ChenM-7/CM-task/blob/master/week3/%E5%9B%BE%E8%A1%A83-%E6%80%A7%E5%88%AB%20infogram.png)

### （五）Chartblocks-条形图

在Excel中分别计算出亚美尼亚每年的自杀人数，导入**Chartblocks**进行可视化，导出图表如下：

![图表4](https://github.com/ChenM-7/CM-task/blob/master/week3/%E5%9B%BE%E8%A1%A84-%E4%BA%BA%E6%95%B0%20Chartblocks.png)

链接：[1990-2016年亚美尼亚自杀死亡人数统计](https://public.chartblocks.com/c/5da6a1023ba0f61240611208?t=8672a1f59b84f46)（有交互效果）

### （六）RAWGraphs-散点图

将亚美尼亚每年的自杀人数和人均GDP结合起来，导入**RAWGraphs**进行可视化。由于涉及年份、人数、人均GDP三个变量，所以采用散点图的方式，横轴表示年份，纵轴表示自杀人数，散点的颜色和大小表示人均GDP，颜色越深、散点越大，人均GDP越高。

![RAWGraphs设置](https://github.com/ChenM-7/CM-task/blob/master/week3/12%20rawgraphs%E8%AE%BE%E7%BD%AE.png)

导出图表如下：

![图表5](https://github.com/ChenM-7/CM-task/blob/master/week3/%E5%9B%BE%E8%A1%A85-GDP%20Rawgraphs2.png)

## 总结

- **工具1：Datawrapper**
  
  图表1：世界地图（可交互）[2012年世界自杀人数统计（部分国家）](https://www.datawrapper.de/_/TIM5U/)
  
  图表2：折线图（kejiaohu）[1990-2016年亚美尼亚男女性自杀人数统计](https://www.datawrapper.de/_/OCRly/)
  
- **工具2：Infogram**
  
  图表3：信息图表（折线图，可交互）[1990-2016年亚美尼亚男女性自杀人数统计](https://infogram.com/yellow-negative-1hnq41mr5rzk43z?live)

- **工具3：Chartblocks**
  
  图表4：条形图（可交互）[1990-2016年亚美尼亚自杀死亡人数统计](https://public.chartblocks.com/c/5da6a1023ba0f61240611208?t=8672a1f59b84f46)
  
- **工具4：RAWGraphs**
  
  图表5：散点图
  
  ![图表5](https://github.com/ChenM-7/CM-task/blob/master/week3/%E5%9B%BE%E8%A1%A85-GDP%20Rawgraphs2.png)
  
  
## 四、使用体会
- 可视化世界博大精深。这周的作业可以说是第一次正式**为我打开了摸索可视化的大门**——以前我只知道Tableau和Adobe系列的PS、AI、AE等，现在第一次发现原来还有其他这么多的可视化工具，其便捷和丰富程度超乎想象，我做图的状态几乎都是这样的：

  > “哇这都可以！(ﾟｰﾟ)” “这么多图表！” “天啊太厉害了！╰(*°▽°*)╯”

  整个过程虽然一边始终在为如何呈现出自己想要的效果而抓狂，一边忍不住感慨真是厉害啊，可视化的世界那么丰富多彩。
  
- 关于数据集：第一次上kaggle找数据的过程是好奇而惊喜的，满脑子想原来这些也可以被做成数据集，比如七季权游中的台词变化，比如鸡尾酒用料和公司大全等等，联系第一周deardata的作业，忽然发现生活和社会中可被收集的“数据”其实远比自己想象的要多。所谓“数据”，也不仅仅是以数字的形式存在，大有可探索的广阔天地。

- 关于自己：

  > “我好菜啊”
  
  真情实感地觉得自己需要学习的东西太多太多了，虽说是数据新闻专业，但大一大二基本都是在“新闻”领域徘徊，关于“数据”，我顶多就是摸了个边，甚至边都没探着，只是远远地看着，嗅到几丝味道，觉得“哦原来是这样”，但事实上还远远不够——每上一次可视化课、每做一次作业都会被打击一次，因为真真切切感受到我的眼界还太窄、知识储备还太不足。所以，接下来还是要冲鸭！给自己充电不能停！

## PS：
- week1、week2的作业已按照老师的要求修改，老师可点击链接直接查看：
  
  [week1 markdown](https://github.com/ChenM-7/CM-task/blob/master/week1/My%20Homework1.md)
  
  [week2 markdown](https://github.com/ChenM-7/CM-task/blob/master/week2/My%20Homework2.md)

- week1-week3的文件也已经按老师的要求整理好啦，每个文件里包括当周的Markdown作业和作业所用到的图片、图表等。

![14](https://github.com/ChenM-7/CM-task/blob/master/week3/14%20github%E6%96%87%E4%BB%B6%E6%95%B4%E7%90%86.png)

### 以上就是本次作业的全部内容 ヾ(￣▽￣)
