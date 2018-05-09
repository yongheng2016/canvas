[https://yuque.com/airing/canvas/readme](https://yuque.com/airing/canvas/readme)

### canvas是行内元素

### 设置画布大小只有两种方法
+ 在canvas标签中设置
+ 在JS代码中更改canvas属性值

### canvas使用：
+ 布置画布：添加`<canvas>`标签元素
+ 获取画布：通过`<canvas>`标签id，获取canvas对象
+ 获取画笔：通过canvas对象的`getContext("2d")`方法，获取2D环境

### canvas绘制都数值都基于px值

### 路径（线、弧形、等）闭合：
> 当你调用`fill()`函数时，所有没有闭合的形状都会自动闭合，所以你不需要调用`closePath()`函数。但是调用`stroke()`时不会自动闭合。

### 绘制图形：(canvas是基于状态的绘制，即向做好绘制计划，最后染色绘制)
+ 移动画笔`moveTo(x,y)`
+ 绘制计划
   + 线段：`lineTo(x,y)`
   + 矩形：`fillRect(x, y, width, height)``strokeRect(x, y, width, height)`
   + 圆弧：`arc(x, y, radius, startAngle, endAngle, anticlockwise)`
     + (x,y)为圆心
     + radius为半径
     + 从startAngle开始到endAngle结束
     + anticlockwise(逆时针))给定方向（默认false，即顺时针）
     + 二次贝塞尔曲线及三次贝塞尔曲线
       + 二次：`quadraticCurveTo(cp1x, cp1y, x, y)`
       + 三次：`bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)`
     + Path2D对象
        + new Path2D();     // 空的Path对象
        + new Path2D(path); // 克隆Path对象
        + new Path2D(d);    // 从SVG建立Path对象
   + SVG paths

### 设置画笔样式
### 确定绘制：
+ `fill()` 填充
+ `stroke()` 描边
