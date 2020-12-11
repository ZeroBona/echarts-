# echarts使用总结

#### 项目介绍
此项目展示使用ehcarts制作柱状图、折线图、饼状图、雷达图、地图、热词云。

#### 使用说明
1. 文件1.html包含内容：柱状图、折线图、饼状图、雷达图
![加载失败](https://raw.githubusercontent.com/ZeroBona/github-img/master/echarts/%E6%9F%B1%E7%8A%B6%E5%9B%BE.png)
2. 文件2.html包含内容：地图展示数据，地图和下拉框之间联动（点击下拉框的省，对应省地图高亮；点击地图上的省，对应下拉框的省选中）
3. 文件3.html包含内容：地图展示全国/省的数据，点击某个省下钻至该省，点击省返回至全国
4. 文件4.html包含内容：地图展示数据，并有图标标注各省数据量
5. 文件5.html包含内容：三种不同的热词云（矩形树图、热词展现、推荐热词）
6. 文件6.html包含内容：简单关系图（一对多）、复杂关系图（神经网络图）

#### echarts与d3对比
1. 对于客户需求要求的图表拥有大量的用户交互场景，用d3比较方便，因为d3中svg画图支持事件处理器，他是基于dom进行操作的。想要实现某个操作，直接调用相关的方法实现效果就行，他那个里面存在链式语法，这个和jQuery的链式调用差不多，简单易读。
2. 对于大量的数据展示并且对于用户交互场景没什么要求，就只是展示数据，那我建议使用echarts，如果使用d3的话展示的每一个数据都是一个标签，那么当数据发生改变的时候这时候图表会重新渲染，会不停的操作dom，操作dom是很耗费性能的。
3. 从兼容性方面考虑：echarts兼容到IE6及以上的所有主流浏览器，而d3兼容IE9及以上以及所有的主流浏览器，如果项目考虑兼容IE6，建议使用echarts。
