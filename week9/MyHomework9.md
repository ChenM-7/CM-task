# week9作业
## 图1：未成年犯罪-白人少年的犯罪数量是所有种族中最多的
- 原图：
  <p>
	  <img src="https://github.com/ChenM-7/CM-task/blob/master/week6/picture/%E5%9B%BE1%20%E6%9C%80%E7%BB%88%E7%89%88-01.jpg" alt="Sample"  width="450" height="600">
	  <p align="center">
	  </p>
  </p>

```r
setwd("~/可视化/week9")
library(readxl)
picture1 <- read_excel("picture1.xlsx")
library(ggplot2)
picture11 <- picture1
picture11$year <- factor(picture1$year)
options(scipen=200)   #取消科学计数法
ggplot(picture11, aes(x=year, y=number, colour=race, group=race)) 
  + geom_line(size=1) 
  + geom_point(size=3) 
  + theme_classic()    #改变背景框的主题
```r

