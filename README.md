这是一个模仿于ios系统的默认样式和效果的城市的三级联动

用法很简单
这是html部门
<div>
    <h1>LArea</h1>
    <div class="content-block">
        <input id="demo1" type="text" readonly="" placeholder="城市选择特效"  value="广东省,广州市,天河区"/>
        <input id="value1" type="hidden"/>
    </div>
    <div class="content-block">
        <input id="demo2" type="text" readonly="" placeholder="城市选择特效" />
        <input id="value2" type="hidden"/>
    </div>
</div>

引入css
<link rel="stylesheet" href="css/LArea.css">

引入两个js文件
<script src="js/LAreaData1.js"></script>
<script src="js/LArea.js"></script>

js部门的编写
var area1 = new LArea();
area1.init({
    'trigger': '#demo1', //触发选择控件的文本框，同时选择完毕后name属性输出到该位置
    'valueTo': '#value1', //选择完毕后id属性输出到该位置
    'keys': {id: 'id',name: 'name'}, //绑定数据源相关字段 id对应valueTo的value属性输出 name对应trigger的value属性输出
    'type': 1, //数据源类型
    'data': LAreaData //数据源
});

这样就可以完成了。。。。。

未完待续，