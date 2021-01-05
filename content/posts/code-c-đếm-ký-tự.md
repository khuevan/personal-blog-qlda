---
path: https://github.com/buixuanthien18it3/NopBaiC/blob/master/DemKyTu.cpp
date: 2021-01-02T08:16:48.561Z
title: "Code C: Đếm Ký Tự"
description: Sử dụng ngôn ngữ để đếm số ký tự trong 1 mảng
---
```js
#include<stdio.h>
#include<conio.h>
#include<string.h>
int main(){
	char Chu\[100];
	printf("Nhap chuoi: ");
	gets(Chu);
	printf("Chuoi vua nhap la: ");
	puts(Chu);
	int Dodai= strlen(Chu);
	printf("So ki tu cua chuoi: %d", Dodai);
}
```