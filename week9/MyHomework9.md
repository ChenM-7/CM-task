# week9作业
## 图1：未成年犯罪-白人少年的犯罪数量是所有种族中最多的
- 原图：
  <p>
	  <img src="https://github.com/ChenM-7/CM-task/blob/master/week6/picture/%E5%9B%BE1%20%E6%9C%80%E7%BB%88%E7%89%88-01.jpg" alt="Sample"  width="450" height="600">
	  <p align="center">
	  </p>
  </p>
  
- R语言制作的图：

  <p>
	  <img src="](https://github.com/ChenM-7/CM-task/blob/master/week9/picture1-1.jpg" alt="Sample"  width="450" height="600">
	  <p align="center">
	  </p>
  </p>
  
- 代码：

```
setwd("~/可视化/week9")
library(readxl)
picture1 <- read_excel("picture1.xlsx")
library(ggplot2)
picture11 <- picture1
picture11$year <- factor(picture1$year)    #把x轴的年份转化为因子变量，不然会出现"2016.4年"这样的情况
options(scipen=200)   #取消科学计数法
ggplot(picture11, aes(x=year, y=number, colour=race, group=race)) 
  + geom_line(size=1) 	#设置折线粗细
  + geom_point(size=3) 	 #加上数据点
  + theme_classic()    #改变背景框的主题
```
## 图2：未成年犯罪-白人少年的犯罪数量是所有种族中最多的
- 原图：
  ![图2.1](https://github.com/ChenM-7/CM-task/blob/master/week4/picture/%E5%9B%BE2.1-%E5%8E%BF%E5%B8%82%E7%BA%A7%E5%A4%84%E7%90%86%E5%8E%82%E7%9A%84%E5%B7%AE%E5%80%BC%E4%B8%8E%E8%AF%A5%E7%9C%81%E4%BB%BDGDP%E6%8A%98%E7%BA%BF%E5%9B%BE.png)
- R语言制作的图

	![picture3.2](https://github.com/ChenM-7/CM-task/blob/master/week9/picture3.2.png)

- 代码：

```
setwd("~/DJ/week9")
library(readxl)
library(ggplot2)
picture3 <- read_excel("picture3.xlsx")
ggplot(picture3, aes(x=Area, y=NumberorGDP, colour=variable, group=variable)) + geom_line(size=1) 
  + geom_point(size=3) 
  + theme_classic()
  + theme(axis.text.x = element_text(angle=45, hjust=1, vjust=1))  #横坐标太密集，如果水平呈现会相互重叠，只好设置一定角度qwq
```
