---
path: https://github.com/buixuanthien18it3/NopBaiC/blob/master/NhapInXuatMangTongGiaiThua.cpp
date: 2021-01-02T08:19:35.218Z
title: "Code C:Nhập In Xuất Mảng "
description: Nhập và xuất mảng trong ngôn ngữ C
---
```js
#include<stdio.h>
#include<conio.h>
void NhapMang(int a[100], int N)
{
	for(int i = 0; i<N; i++)
	{
		{
			printf("a[%d] ",i);
			scanf("%d",&a[i]);
		}
	}
}
void XuatMang(int a[100], int N)
{
	for(int i = 0; i<N; i++)
	{
		{
			printf("gia tri %d :%d \n",i+1,a[i]);
		}
	}
}
int GiaiThua(int N)
{	int gt=1;
	for(int j=1; j<=N; j++)
	{
		gt=gt*j;
	}
	return gt;
}

float TinhTong(int a[100], int N)
{
	int tong=0;
	float gt;
	for(int j=0; j<N; j++)
	{
		gt=GiaiThua(a[j]);
		tong=tong+gt;
	}
	printf("%d",tong);
}
int main()
{
	int N;
	int a[100];
	printf("Tinh Tong Cac Giai Thua");
	printf("Nhap so phan tu: \n");
	scanf("%d",&N);
	printf("Nhap Gia Tri Cho Mang:\n"); NhapMang(a,N);
	printf("Cac Gia Tri Ban Vua Nhap la:\n"); XuatMang(a,N);
	printf("Tong Cac Giai Thua Cac Gia Tri Ban Vua Nhap La: "); TinhTong(a,N);
}
```

Còn nhiều cách giải khác nhé. IT Blog sẽ cập nhập thêm