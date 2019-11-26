# week9作业
## 图1：

```r
setwd("~/可视化/week9")
library(readxl)
picture1 <- read_excel("picture1.xlsx")
View(picture1)
library(ggplot2)
picture11 <- picture1
picture11$year <- factor(picture1$year)
options(scipen=200)
ggplot(picture11, aes(x=year, y=number, colour=race, group=race)) + geom_line(size=1) + geom_point(size=3) + theme_bw()
```r

