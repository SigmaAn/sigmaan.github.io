---
layout: post
title:  "快速排序"
categories: jekyll update
---
快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序快速排序

```cpp
/*
* @author lianera
* @date 2016-2-17 19:28:32
* @brief quick soft
* O(nlogn)
*/
#include <iostream>

template<typename T>
void swap(T& a, T&b)
{
	T t = a;
	a = b;
	b = t;
}

template<typename T>
int partition(T a[], int p, int q)
{
	int i = p - 1;
	int k = q;
	for(int j = p; j < q; j++){
		if(a[j] < a[k]){
			i++;
			swap(a[i], a[j]);
		}
	}
	swap(a[i + 1], a[k]);
	return i + 1;
}

template<typename T>
void quick_sort(T a[], int p, int q)
{
	if(p < q){
		int k = partition(a, p, q);
		quick_sort(a, p, k - 1);
		quick_sort(a, k + 1, q);
	}
}

int main()
{
	int a[] = {24,54,32,-56,12,-6,543,23,-85,32,6,65};
	const int sa = sizeof(a) / sizeof(int);
	char b[] = { 'd', 'c', 'r', 's', 'j', 't' };
	const int sb = sizeof(b) / sizeof(char);
	float c[] = { 4.32f, 5.4f, 0.01f, -56.9f, 54.34f, -34.54f };
	const int sc = sizeof(c) / sizeof(float);
	long d[] = { 1 };
	quick_sort(a, 0, sa - 1);
	quick_sort(b, 0, sb - 1);
	quick_sort(c, 0, sc - 1);
	quick_sort(d, 0, 0);
	for (int i = 0; i < sa; i++)
		std::cout << a[i] << ' ';
	std::cout << std::endl;
	for (int i = 0; i < sb; i++)
		std::cout << b[i] << ' ';
	std::cout << std::endl;
	for (int i = 0; i < sc; i++)
		std::cout << c[i] << ' ';
	std::cout << std::endl;
	std::cout << d[0] << std::endl;
	return 0;
}

```