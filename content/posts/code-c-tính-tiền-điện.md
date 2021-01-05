---
path: https://github.com/buixuanthien18it3/NopBaiC/blob/master/TinhTienDien.cpp
date: 2021-01-02T08:21:21.276Z
title: "Code C: Tính Tiền Điện"
description: Code C tính tiền điện với nhập số điện
---
Số điện được nhập vào, nếu dưới 50 số \*1500, từ 50 đến 100 \*2000, trên 1000 * 2500 

```js
#include<stdio.h>
#include<conio.h>
int TienDien(int somoi, int socu)
{
	int tien = 0;
	int sodien= somoi-socu;
	int kq;
	if(sodien<50)  tien= sodien*1500;
	else if(sodien>=50 && sodien<=100) tien= 49*1500+(sodien-49)*2000;
	else tien=49*1500+50*2000+((sodien-99)*2500);
	return tien;
}
int main(){
	int diencu, dienmoi;
	printf("Bai toan tinh tien dien: ");
	printf("\nNhap so dien cu: ");
	scanf("%d", &diencu);
	printf("Nhap so dien moi: ");
	scanf("%d",&dienmoi);
	if(diencu>dienmoi) 
	printf("Ban Da Nhap Sai");
	else
	printf("So tien dien cua ban phai tra la: %d VND ", TienDien(dienmoi, diencu));
}
```