---
layout: post
title:  "二分法查找"
categories: jekyll update
---
二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找二分法查找


```cpp
#include <iostream>

const int NIL = -1;
/**
* binary search
* O(logn)
*/
template <typename T>
int binary_search(T A[], int length, int k)
{
	int p = 0;
	int r = length - 1;
	while (p <= r){
		int q = p + (r - p) / 2;
		if (A[q] > k)
			r = q - 1;
		else if (A[q] < k)
			p = q + 1;
		else
			return q;
	}
	return NIL;
}

int main()
{
	const int intarr[] = { 2, 4, 7, 9, 15, 18, 35, 57, 89, 96 };
	const char charr[] = {'a','d','f','g','j','p','u','y','z'};
	const int intval[] = {1};
	int p1 = binary_search(intarr, sizeof(intarr) / sizeof(int), 34);
	int p2 = binary_search(charr, sizeof(charr) / sizeof(char), 'f');
	int p3 = binary_search(intval, sizeof(intval) / sizeof(int), 1);
	std::cout << p1 << std::endl << p2 << std::endl << p3 << std::endl;
	return 0;
}

```