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
In the last episode we talked about the data representation of integer, a kind
of fixed-point numbers. Today we're going to learn about floating-point numbers. 

Floating-point numbers are used to _approximate_ real numbers. Because of the 
fact that all the stuffs in computers are, eventually, just a limited sequence 
of bits. The representation of floating-point number had to made trade-offs 
between _ranges_ and _precision_.

Due to its computational complexities, CPU also have a dedicated set of 
instructions to accelerate on floating-point arithmetics. 
<!-- 정리 텍스트 end -->

Terminologies
-------------


The terminologies of floating-point number is coming from the 
[_scientific notation_](https://en.wikipedia.org/wiki/Scientific_notation), 
where a real number can be represented as such:

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