### canvas实现时钟问题分解

1.绘制表盘，数字的位置计算（圆周坐标）

2.时分秒针旋转（秒针旋转时，分针和时针也会动+ js时间对象相关）



### 圆周坐标问题

如何确定（x,y） <= 根据半径r和角度,cos,sin数学运算

### 涉及到的canvas操作

##### ctx.save()、ctx.store()

- save之后，可以调用Canvas的平移、放缩、旋转、错切、裁剪等操作。

- restore：用来恢复Canvas之前保存的状态。防止save后对Canvas执行的操作对后续的绘制有影响。

-   如果不对canvas进行save以及restore，那么每一次绘图都会在上一次的基础上进行操作，最后导致错位。（比如说你相对于起始点每次30度递增旋转，30，60，90.      如果不使用save 以及 restore 就会变成30, 90, 150，每一次在前一次基础上进行了旋转。save是入栈，restore是出栈）

##### ctx.translate(x,y) 平移坐标系 

- 主要目的是把坐标原点平移到圆心后，方便绘制以及表针旋转。
- ![img](https://mdn.mozillademos.org/files/234/Canvas_grid_translate.png)

##### ctx.rotate(angle) 旋转画布

旋转中心点一直是 canvas 的起始点。 如果想改变中心点，我们可以通过 [`translate()`](https://developer.mozilla.org/zh-CN/docs/Web/API/CanvasRenderingContext2D/translate) 方法移动 canvas

`ctx.beginPath() ctx.moveTo() ctx.lineTo() ctx.arc() ctx.fill()`

ctx.fillStyle = \`rgb(${Math.random()*255},${Math.random()*255},${Math.random()*255})`;





