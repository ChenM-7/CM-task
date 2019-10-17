# 第三周作业
## 本次作业主要分为四块内容：可视化工具整理、数据集、对数据集的可视化呈现、使用体会。

## 一、国内外免费图表制作工具整理
- **RAWGraphs** [https://rawgraphs.io/](https://rawgraphs.io/)
  
  【01】
    在线可视化工具

  图表类型很丰富，除了常见的柱状图、散点图外，还包括其他一些很神奇的图表（如下图）【02】
  
  除了可以生成常规的png格式图片，还可以生成SVG代码（！），便于直接复制到网页代码中呈现可视化效果。
  
- **ChartBlocks** [https://www.chartblocks.com/en/](https://www.chartblocks.com/en/)
  
  【03】在线可视化工具
  
- **Datawrapper** [https://www.datawrapper.de/](https://www.datawrapper.de/)（在线）

  【04】
  
  除了图表还可以制作交互式地图！无法免费下载，但可以用网页形式分析。
  
- **Infogram** [https://infogram.com/](https://infogram.com/)（在线）
  
  除了可以制作图表外，还有多种信息图表排版可供选择！（太方便了吧！）
  
  【图05】
    
 无法免费下载，但可以以网页形式分享，保持了交互的特性！
  
- **Tableau**
  
  可以免费申请学生版，操作比前面的在线工具更加复杂，但功能也更强大。
  
- **Python**

  这就得靠码代码了，可以利用如pandas和matplotlib等库进行可视化制作。

- **D3.js**

   一个资源丰富的开源的JavaScript函数库，从上一届师哥师姐了解到，他们的很多作品可视化的实现都少不了D3.js的帮助。

- **Echartshttps**[www.echartsjs.com/zh/index.html](www.echartsjs.com/zh/index.html)

  也是一个纯javascript的数据可视化库。
 
- **Excel**

  Excel虽然看起来很朴素（？），但也是一款很实在的图表制作软件！（大一不会做好看的数据图，那时候写社会调查报告时用的图表就都来自Excel hhhh)
  
- **AI+PS**

  可以直接用来做图表，也可以把从其可视化工具（如tableau）中做出来的图表拖进去进一步完善。
  
  
## 二、数据集

【06】
“1985年至2016年自杀率概述——按年份和国家比较社会经济信息和自杀率”

这是我从kaggle中选取的数据集，选择时主要考虑了以下几点：

1. **内容**：
  
  如下图，这个自杀数据集除了包括国家、自杀人数之外，还进行了性别、年龄的进一步划分，此外还试图将自杀数据和社会经济发展情况相结合，这个切入点很有意思。“自杀”这一社会行为背后映射出的不仅仅是个人性格和际遇，还有整个社会环境的变化。
  【图10】
  
  这是对数据集内容的描述和数据来源（参考文献）：【图09】

2. **usability（易用性/可用程度）**：

  kaggle对usability的描述如下，符合越多项，可用程度越高。
  
  【08】

  本数据集的易用性为7.1，在kaggle中大概处于中等偏上的位置，虽然没有达到最高（10.0），但一方面我觉得用来做本次的数据呈现已经足够，另一方面我个人对这一话题的也很感兴趣hhh，两相结合最终选择了这个“自杀数据集”。
  
## 三、可视化呈现

### 过程
#### （一）
首先下载数据集，在Excel里顺利打开，一共有27820条数据，变量包括国家、年份、性别、年龄、自杀人数、该年龄和性别对应的总人口、国家全年GDP和人均GDP等。
  
【11】

#### （二）datawrapper-世界地图
粗略浏览了一下，我发现这一数据集包括了81个国家，同时并不是每个国家都有完整的从1985-2016所有年份的自杀数据，比较了一下之后我选择了2012年的数据，这一年的数据相对全面。在excel中筛选出各国2012年的数据，分别用求和公式（SUM）算出自杀的总人数（整个过程大概花了三十分钟,可能是本小白还不太熟练excel吧/捂脸）。

把数据填进**datawrapper**，前面有说，这个在线工具可以直接做可视化地图！虽然不能直接免费下载，但可以生成可交互的网页链接（可视化小白表示非常惊喜⊙▽⊙）！

链接：[2012年世界自杀人数统计（部分国家）](https://www.datawrapper.de/_/TIM5U/)

效果如下（截图）：【图表1】

#### （三）datawrapper-折线图

那么单个国家的自杀情况如何呢？本来想以美国为例进行说明，但发现自杀人数基数太大了，用图表呈现很难体现出差别和变化，于是转而找了一个小国家——亚美尼亚（Armenia）。具体情况如下：

继续用**datawrapper**——在Excel中计算出1990-2016男性和女性自杀人数，这次用图表来呈现：

链接：[1990-2016年亚美尼亚男女性自杀人数统计](https://www.datawrapper.de/_/OCRly/)（有交互效果）

效果如下（截图）：【图表2】

#### （四）Infogram-折线图+信息图表

  继续探索，我又发现了一个神奇的在线可视化工具——**Infogram**！不仅可以做各种图表，还有各种排版模板（排版小白的生命之光）！

  正好在里面发现了一个适合“性别”的图表排版，于是继续用前面的数据。

  链接：[1990-2016年亚美尼亚男女性自杀人数统计](https://infogram.com/yellow-negative-1hnq41mr5rzk43z?live)（有交互效果）

  效果如下（截图）：【图表3】

### （五）Chartblocks-条形图

在Excel中分别计算出亚美尼亚每年的自杀人数，导入**Chartblocks**进行可视化，导出图表如下：
【图表4】

链接：[1990-2016年亚美尼亚自杀死亡人数统计](https://public.chartblocks.com/c/5da6a1023ba0f61240611208?t=8672a1f59b84f46)（有交互效果）

### （六）RAWGraphs-散点图

将亚美尼亚每年的自杀人数和人均GDP结合起来，导入**RAWGraphs**进行可视化

<svg width="847" height="500" xmlns="http://www.w3.org/2000/svg"><g transform="translate(40,20)"><g class="x axis" transform="translate(0,440)" fill="none" font-size="10" font-family="sans-serif" text-anchor="middle" style="stroke-width: 1px; font-size: 10px; font-family: Arial, Helvetica;"><path class="domain" stroke="#000" d="M0.5,-440V0.5H787.5V-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></path><g class="tick" opacity="1" transform="translate(0.5,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">1,990</text></g><g class="tick" opacity="1" transform="translate(61.03846153846154,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">1,992</text></g><g class="tick" opacity="1" transform="translate(121.57692307692308,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">1,994</text></g><g class="tick" opacity="1" transform="translate(182.1153846153846,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">1,996</text></g><g class="tick" opacity="1" transform="translate(242.65384615384616,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">1,998</text></g><g class="tick" opacity="1" transform="translate(303.19230769230774,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,000</text></g><g class="tick" opacity="1" transform="translate(363.7307692307692,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,002</text></g><g class="tick" opacity="1" transform="translate(424.2692307692308,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,004</text></g><g class="tick" opacity="1" transform="translate(484.8076923076923,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,006</text></g><g class="tick" opacity="1" transform="translate(545.3461538461538,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,008</text></g><g class="tick" opacity="1" transform="translate(605.8846153846155,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,010</text></g><g class="tick" opacity="1" transform="translate(666.4230769230769,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,012</text></g><g class="tick" opacity="1" transform="translate(726.9615384615385,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,014</text></g><g class="tick" opacity="1" transform="translate(787.5,0)"><line stroke="#000" y2="-440" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" y="3" dy="0.71em">2,016</text></g></g><g class="y axis" fill="none" font-size="10" font-family="sans-serif" text-anchor="end" style="stroke-width: 1px; font-size: 10px; font-family: Arial, Helvetica;"><path class="domain" stroke="#000" d="M787,440.5H0.5V0.5H787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></path><g class="tick" opacity="1" transform="translate(0,400.5)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">60</text></g><g class="tick" opacity="1" transform="translate(0,343.3571428571429)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">70</text></g><g class="tick" opacity="1" transform="translate(0,286.2142857142857)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">80</text></g><g class="tick" opacity="1" transform="translate(0,229.07142857142858)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">90</text></g><g class="tick" opacity="1" transform="translate(0,171.92857142857144)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">100</text></g><g class="tick" opacity="1" transform="translate(0,114.78571428571428)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">110</text></g><g class="tick" opacity="1" transform="translate(0,57.64285714285717)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">120</text></g><g class="tick" opacity="1" transform="translate(0,0.5)"><line stroke="#000" x2="787" style="shape-rendering: crispedges; fill: none; stroke: rgb(204, 204, 204);"></line><text fill="#000" x="-3" dy="0.32em">130</text></g></g><g class="circle"><circle transform="translate(0, 211.42857142857144)" r="9.117259898320413" style="fill: rgb(189, 200, 217); fill-opacity: 0.9;"></circle><text transform="translate(0, 211.42857142857144)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">93</text></g><g class="circle"><circle transform="translate(30.26923076923077, 285.7142857142857)" r="8.468588656082318" style="fill: rgb(195, 206, 221); fill-opacity: 0.9;"></circle><text transform="translate(30.26923076923077, 285.7142857142857)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">80</text></g><g class="circle"><circle transform="translate(60.53846153846154, 268.57142857142856)" r="6.792671738633186" style="fill: rgb(208, 219, 230); fill-opacity: 0.9;"></circle><text transform="translate(60.53846153846154, 268.57142857142856)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">83</text></g><g class="circle"><circle transform="translate(90.8076923076923, 137.14285714285717)" r="6.5780533252275895" style="fill: rgb(209, 220, 231); fill-opacity: 0.9;"></circle><text transform="translate(90.8076923076923, 137.14285714285717)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">106</text></g><g class="circle"><circle transform="translate(121.07692307692308, 102.85714285714283)" r="6.807698149711737" style="fill: rgb(207, 218, 230); fill-opacity: 0.9;"></circle><text transform="translate(121.07692307692308, 102.85714285714283)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">112</text></g><g class="circle"><circle transform="translate(151.34615384615387, 0)" r="7.093311116870078" style="fill: rgb(205, 216, 229); fill-opacity: 0.9;"></circle><text transform="translate(151.34615384615387, 0)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">130</text></g><g class="circle"><circle transform="translate(181.6153846153846, 245.71428571428572)" r="7.318024310863368" style="fill: rgb(204, 215, 228); fill-opacity: 0.9;"></circle><text transform="translate(181.6153846153846, 245.71428571428572)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">87</text></g><g class="circle"><circle transform="translate(211.8846153846154, 302.8571428571429)" r="7.366123069481127" style="fill: rgb(204, 215, 227); fill-opacity: 0.9;"></circle><text transform="translate(211.8846153846154, 302.8571428571429)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">77</text></g><g class="circle"><circle transform="translate(242.15384615384616, 365.7142857142857)" r="7.809329811153534" style="fill: rgb(200, 211, 225); fill-opacity: 0.9;"></circle><text transform="translate(242.15384615384616, 365.7142857142857)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">66</text></g><g class="circle"><circle transform="translate(272.4230769230769, 360)" r="7.6996508193276325" style="fill: rgb(201, 212, 226); fill-opacity: 0.9;"></circle><text transform="translate(272.4230769230769, 360)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">67</text></g><g class="circle"><circle transform="translate(302.69230769230774, 394.2857142857143)" r="7.796518266764145" style="fill: rgb(200, 211, 225); fill-opacity: 0.9;"></circle><text transform="translate(302.69230769230774, 394.2857142857143)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">61</text></g><g class="circle"><circle transform="translate(332.96153846153845, 400)" r="8.152660376301645" style="fill: rgb(197, 208, 223); fill-opacity: 0.9;"></circle><text transform="translate(332.96153846153845, 400)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">60</text></g><g class="circle"><circle transform="translate(363.2307692307692, 320)" r="9.287273320131828" style="fill: rgb(187, 198, 216); fill-opacity: 0.9;"></circle><text transform="translate(363.2307692307692, 320)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">74</text></g><g class="circle"><circle transform="translate(393.5, 405.7142857142857)" r="9.993371667231045" style="fill: rgb(180, 191, 212); fill-opacity: 0.9;"></circle><text transform="translate(393.5, 405.7142857142857)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">59</text></g><g class="circle"><circle transform="translate(484.3076923076923, 297.1428571428571)" r="15.18909000709199" style="fill: rgb(112, 125, 166); fill-opacity: 0.9;"></circle><text transform="translate(484.3076923076923, 297.1428571428571)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">78</text></g><g class="circle"><circle transform="translate(514.5769230769231, 337.1428571428571)" r="18.127958794820362" style="fill: rgb(60, 79, 132); fill-opacity: 0.9;"></circle><text transform="translate(514.5769230769231, 337.1428571428571)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">71</text></g><g class="circle"><circle transform="translate(544.8461538461538, 382.8571428571429)" r="19.268009839230942" style="fill: rgb(34, 60, 117); fill-opacity: 0.9;"></circle><text transform="translate(544.8461538461538, 382.8571428571429)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">63</text></g><g class="circle"><circle transform="translate(575.1153846153845, 440)" r="17.73936743184606" style="fill: rgb(68, 86, 136); fill-opacity: 0.9;"></circle><text transform="translate(575.1153846153845, 440)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">53</text></g><g class="circle"><circle transform="translate(605.3846153846155, 325.7142857142857)" r="18.365472438938216" style="fill: rgb(55, 75, 129); fill-opacity: 0.9;"></circle><text transform="translate(605.3846153846155, 325.7142857142857)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">73</text></g><g class="circle"><circle transform="translate(635.6538461538462, 360)" r="19.193909657461013" style="fill: rgb(36, 61, 118); fill-opacity: 0.9;"></circle><text transform="translate(635.6538461538462, 360)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">67</text></g><g class="circle"><circle transform="translate(665.9230769230769, 291.42857142857144)" r="19.133930890495982" style="fill: rgb(37, 62, 119); fill-opacity: 0.9;"></circle><text transform="translate(665.9230769230769, 291.42857142857144)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">79</text></g><g class="circle"><circle transform="translate(696.1923076923076, 360)" r="19.570841305363384" style="fill: rgb(25, 55, 113); fill-opacity: 0.9;"></circle><text transform="translate(696.1923076923076, 360)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">67</text></g><g class="circle"><circle transform="translate(726.4615384615385, 411.42857142857144)" r="20" style="fill: rgb(8, 48, 107); fill-opacity: 0.9;"></circle><text transform="translate(726.4615384615385, 411.42857142857144)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">58</text></g><g class="circle"><circle transform="translate(756.7307692307693, 320)" r="19.13873649039232" style="fill: rgb(37, 62, 119); fill-opacity: 0.9;"></circle><text transform="translate(756.7307692307693, 320)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">74</text></g><g class="circle"><circle transform="translate(787, 360)" r="19.169941909396012" style="fill: rgb(36, 62, 118); fill-opacity: 0.9;"></circle><text transform="translate(787, 360)" text-anchor="middle" dy="15" style="font-size: 10px; font-family: Arial, Helvetica;">67</text></g><g class="point"><circle transform="translate(0, 211.42857142857144)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(30.26923076923077, 285.7142857142857)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(60.53846153846154, 268.57142857142856)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(90.8076923076923, 137.14285714285717)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(121.07692307692308, 102.85714285714283)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(151.34615384615387, 0)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(181.6153846153846, 245.71428571428572)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(211.8846153846154, 302.8571428571429)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(242.15384615384616, 365.7142857142857)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(272.4230769230769, 360)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(302.69230769230774, 394.2857142857143)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(332.96153846153845, 400)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(363.2307692307692, 320)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(393.5, 405.7142857142857)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(484.3076923076923, 297.1428571428571)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(514.5769230769231, 337.1428571428571)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(544.8461538461538, 382.8571428571429)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(575.1153846153845, 440)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(605.3846153846155, 325.7142857142857)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(635.6538461538462, 360)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(665.9230769230769, 291.42857142857144)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(696.1923076923076, 360)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(726.4615384615385, 411.42857142857144)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(756.7307692307693, 320)" r="1" style="fill: rgb(0, 0, 0);"></circle></g><g class="point"><circle transform="translate(787, 360)" r="1" style="fill: rgb(0, 0, 0);"></circle></g></g></svg>
