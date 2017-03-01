

# ��ʼ #


canvas ���ĵ�˵���� �������ߵ�
http://www.w3school.com.cn/tags/html_ref_canvas.asp

## ���� ##

```
<body>

  <canvas width="500" height="300" id="c"></canvas>

</body>

```


## ���� ##

```
//����һ������
var canvas = document.getElementById("c");

//��ȡһֻ����
var paint = canvas.getContext("2d");

paint.strokeStyle = "black";

paint.beginPath();
paint.lineTo(0,0);
paint.lineTo(100,100);
paint.stroke();

```

������÷�
lineCap �������û򷵻�����ĩ����ñ����ʽ��
ע�ͣ�"round" �� "square" ��ʹ������΢�䳤��

---------

## ���� ##

arc
x	Բ�����ĵ� x ���ꡣ
y	Բ�����ĵ� y ���ꡣ
r	Բ�İ뾶��
sAngle	��ʼ�ǣ��Ի��ȼơ�������Բ�ε�������λ���� 0 �ȣ���
eAngle	�����ǣ��Ի��ȼơ�
counterclockwise	��ѡ���涨Ӧ����ʱ�뻹��˳ʱ���ͼ��False = ˳ʱ�룬true = ��


```
//��ȡһֻ����
var paint = canvas.getContext("2d");

paint.fillStyle="red";
	//��ʼ��Բ
paint.beginPath();
// ����һ����������Բ��  ���������뾶 �����ģ���ʼ�ĽǶ�  �����壺�����ĽǶ�  ������������˳��
paint.arc(x, y, 10, 0, Math.PI * 2, false);
paint.closePath();

//����ԲΪʵ�ĵ�
paint.fill();
```

## ���� ##

```
context.strokeRect(origin.x,origin.y,size.width,size.height);

context.fill();
```


## ���� ##



```
context.restore();
context.fillText(text,origin.x,origin.y,maxWidth);
```



## ͼƬ ##

drawImage
img	�涨Ҫʹ�õ�ͼ�񡢻�������Ƶ��
sx	��ѡ����ʼ���е� x ����λ�á�
sy	��ѡ����ʼ���е� y ����λ�á�
swidth	��ѡ��������ͼ��Ŀ�ȡ�
sheight	��ѡ��������ͼ��ĸ߶ȡ�
x	�ڻ����Ϸ���ͼ��� x ����λ�á�
y	�ڻ����Ϸ���ͼ��� y ����λ�á�
width	��ѡ��Ҫʹ�õ�ͼ��Ŀ�ȡ�����չ����Сͼ��
height	��ѡ��Ҫʹ�õ�ͼ��ĸ߶ȡ�����չ����Сͼ��

```
var image = new Image();
image.src = imagePath;
image.onload = function () {
    context.drawImage(image,cutOrigin.x,cutOrigin.y,cutSize.width,cutSize.height,origin.x,origin.y,size.width,size.height);
}
```

## �������ͼ�� ##

```
//��� ���Ƶ�����
//x,yԭ��
//w,h�������Ŀ�� �͸߶�
context.clearRect(100,100,700,700);
```

# ����Ч��С���� #

## ҳ���Ⱥ͸߶� ##

```
window.innerWidth ��ȡҳ��Ŀ��
window.innerHeight ҳ��ĸ߶�
```

# ���ʰ��� #

## ����֪ʶ ##

### �¼����� ###

clientX/Y��ȡ�����Ǵ������������������������ϽǾ��룬����ҳ��������ı�

pageX/Y��ȡ�����Ǵ���������ĵ��������ϽǾ��룬������ҳ��������ı�

�����ԣ���IE6/7/8��֧���⣬�����������֧��

---------

### �ı��ߵ���ɫ ###

```
var lineColor = document.querySelector(".lineColor");

lineColor.onchange = function () {
    painter.setLineColor(this.value);
}

```

### ����ͼ����״ ###

```
// css ������
cursor: crosshair;

// js ������
self.target.style.cursor = "crosshair";


```

���������ͼ��˵��
http://www.w3school.com.cn/cssref/pr_class_cursor.asp



# ̫��ͼ�� #

�����ȣ���Բ��

![](doc/snap/1.png)
