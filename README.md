
# ����֪ʶ #




## ҳ���Ⱥ͸߶� ##

```
window.innerWidth ��ȡҳ��Ŀ��
window.innerHeight ҳ��ĸ߶�
```


## ���� ##

��ͼ

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
