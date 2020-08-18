---
title: "프로그래밍 시작하기"
subtitle: "파이썬 입문"
layout: post
author: "Hux"
header-style: text
tags:
  - Python
  - 딥러닝
  - 데이터 분석
---
<!-- 정리 텍스트 -->

<!-- 정리 텍스트 end -->

교육용 프로그래밍 언어
-------------



번역 프로그램
-------------


<!-- code -->
```
1.2345 = 12345 × 10 ** -4
         -----   --    --
  significand^   ^base  ^exponent
```
<!-- code end-->

<!-- code scroll -->
```cpp
       (8 bits)             (23 bits)
sign   exponent             fraction 
  0   011 1111 1    000 0000 0000 0000 0000 0000

 31   30 .... 23    22 ....................... 0
```
<!-- code scroll end-->

- _significand_, or _mantissa_, 有效数字, 尾数
- _base_, or _radix_ 底数
- _exponent_, 幂

So where is the _floating point_? It's the `.` of `1.2345`. Imaging the dot
can be float to the left by one to make the representation `.12345`.

The dot is called _radix point_, because to us it's seem to be a _decimal point_,
but it's really a _binary point_ in the computers.

Now it becomes clear that, to represent a floating-point number in computers,
we will simply assign some bits for _significand_ and some for _exponent_, and
potentially a bit for _sign_ and that's it.

References
----------

- <https://en.wikipedia.org/wiki/Floating-point_arithmetic>
- <https://www3.ntu.edu.sg/home/ehchua/programming/java/datarepresentation.html>