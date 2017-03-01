
# 基础知识 #




## 页面宽度和高度 ##

```
window.innerWidth 获取页面的宽度
window.innerHeight 页面的高度
```


## 画笔 ##

画图

```
//获取一只画笔
var paint = canvas.getContext("2d");

paint.fillStyle="red";
	//开始画圆
paint.beginPath();
// 参数一，参数二：圆点  参数三：半径 参数四：开始的角度  参数五：结束的角度  参数六：画的顺序
paint.arc(x, y, 10, 0, Math.PI * 2, false);
paint.closePath();
//设置圆为实心的
paint.fill();
```
