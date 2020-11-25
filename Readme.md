This is a Git Repository.
Modified readme file.
Still Modified readme.

# Forming a Magic Square

将三维数组拆分为一个length为9的数组，进行**排列**后得到所有的3x3矩阵情况

***如何排列？***

**用二叉树解决排列**

```

```



再根据行列相加是否相等判断是否为Magic Square

arr[0] + arr[3] + arr[6] //第一列

arr[1] + arr[4] + arr[8] //第二列

arr[2] + arr[5] + arr[8] //第三列

```Jav
int[] resCol;
int[] resLine;
int t = 0;
for(i = 0; i < 3; i++){
	// 列相加结果
	resCol[i] = arr[i] + arr[i + 3] + arr[i + 6];
}
for(i = 0; i < 6; i = i + 3){
	// 行相加结果
	resLine[t] = arr[i] + arr[i + 1] + arr[i + 2];
	t++;
}
// 正向反向斜线
resZ = arr[0] + arr[4] + arr[8];
resF = arr[2] + arr[4] + arr[6];
```

**如何判断位置改变来计算cost?**