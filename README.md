# Data Visualization

Make Effective Data Visualization with D3 by Sunshine Yang

## 概要
1. 本次数据可视化项目使用数据为Prosper贷款数据，Prosper是美国一家不同于传统借贷的 P2P 借贷服务的公司，数据集中包括Prosper公司2005至2014年的贷款数据。
2. 本次可视化主要观察从2005年至2014年该公司贷款总金融的变化(linechart),发现整体上承逐年上升趋势。但是2008-2009年贷款金额最低，猜测有可能是因为2008金融危机所致。2013年该公司贷款总金额达到最高值
3. 同时通过 D3 来展示各年度中贷款额度与贷款人所在州分布情况

## 设计

该项目的目的是希望能够通过数据可视化呈现不同年份中Prosper公司贷款额度的变化，除此之外，希望能够在最终可视化交互过程中呈现出各州是否有发生贷款；在指定年份中，呈现各月份中贷款变化趋势以及贷款人所在州的分布情况

在设计交互过程中，考虑信息传达的真实性(非作者偏差)，以及项目中使用的数据是数值类型的，
* 使用点位置，条形图的高度来表现数据大小的量 
* 因为需要表现出数据整体变化趋势，使用折线图来表现出不同年份的数据动态变化趋势；
* 为了增强读者交互性，使用了颜色变化来的可视化编码并且增加了年份filter帮助读者观察某一年贷款数据
* 最后，为了传达出图形的数据内容，使用了文本内容直接表现出数据的内容。

## 文件结构
* getdata.py

	>选择需要可视化的相关变量
* index.html

	>最终D3可视化的HTML文件
* data 

	>本次项目的数据文件
	>> 使用了两个数据集，dataset.csv 包含了贷款总金融的数据集， statetopo.js 文件是用于制作美国各州地图的数据集
* js 

	>使用到的 JavaScript 文件
	
* css 
	>使用到的Bootstrap及自定义的css文件

## 反馈

### 反馈1 

1. 页面布局问题，利用 bootstrap进行页面布局中，存在因分辨率问题不能够很好展现可视化结果。通过更改 CSS 文件和利用 bootstrap 的栅栏格式进行了相应的修改
2. 页面上的按钮及linechart的标题不够明确
3. 需要辅助文本信息解释图表，提供简洁的文字描述作为补充

### 反馈2

1. 提供刷选器功能，筛选某一年份贷款总额变化及对应的贷款用户所在州分布情况，提供读者可视化图表的交互
2. 地图使用的颜色亮度过高，建议重新选择一些user-friendly的颜色
3. 坐标轴单位不够简洁准确

### 反馈3

1. 通过年份筛选器后，X轴的tick需要更新，因为X轴标题为Date，建议直方图中X轴标记年份
2. 直方图无具体数字标识，建议当用户鼠标Hover时，bin上方展示具体数值或提供额外的数值信息


## 参考
1. http://www.perceptualedge.com/blog/?p=1374
2. https://d3js.org/
3. https://iros.github.io/d3-v4-whats-new/#1
4. https://bl.ocks.org/mbostock/3883245
5. https://github.com/d3/d3-geo/blob/master/README.md#transforms
6. https://bl.ocks.org/Andrew-Reid/496078bd5e37fd22a9b43fd6be84b36b
7. http://hugo.qov.tw/?p=1185&i=1
8. https://codeday.me/bug/20170326/6296.html
9. https://bl.ocks.org/mbostock/3259783
10. https://bl.ocks.org/d3noob/bdf28027e0ce70bd132edc64f1dd7ea4
11. https://bl.ocks.org/hhhuangqiong/ffa47c3f432f2f4cd750e421b075beca
12. https://bl.ocks.org/d3noob/bdf28027e0ce70bd132edc64f1dd7ea4
13. http://v3.bootcss.com
14. http://api.jquery.com
15. http://dovov.com/bootstrapless.html
