### 炫彩小球实现效果：

鼠标移动产生小球，鼠标移开的轨迹上小球散开并消失

### 思路分析：

1.触发与记录：鼠标移动触发新建小球（随机半径，event事件获取坐标）；使用数组记录小球们；

2.小球怎么散开： 需要随机xy偏移量

3.小球怎么消失：通过判断半径<0，来移除小球

4.动态效果:

定时器定时渲染小球，每秒更新数组里的所有小球大小并清空画板绘制出来



