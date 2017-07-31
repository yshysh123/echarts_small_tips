# echarts_small_tips
echarts的一个小技巧
Echarts有一个坑爹的地方，就是高度宽度不能给百分比。
所以我们只能在JS里面或者行间写宽高，所以导致无法自适应屏幕宽高或者容器宽高。
但是JQ给我们提供了一个不错的方法。就是resize()。
但直接调用没有起作用，引入jquery.ba-resize.js文件就可以了。
    
   

``` xml
<script type="text/javascript" src="js/jquery-1.4.2.js"></script> 
<script type="text/javascript" src=js/jquery.resizable.js></script> 
```

``` gams
<div class="chart" >
   <div id="myChart" style="height:300px"></div>
</div>
var myChart = Echarts.init(document.getElementById("myChart"));
$('.chart').resize(function () {
   myChart.resize();
});
```
