In this problem after continuing calculations we can find that any number decomposed into smaller
numbers will always result in a higher multiplication after such number goes above 4

Example:
+ 2 decomposes into 1+1 --- 1x1
+ 3 into 2+1 --- 2x1
+ 4 into 2+2 --- 2x2

But at the point we reach 5 or any subsequent number we can always decompose it further to have a greater product
+ 6 could be 2+2+2 but we know that 2x2x2 is less than 3x3

Following this we know that the furthest something can be decomposed into we need to know a previous number that
can decomposed but also can have a 3 added to it, giving ur our new number.

Example:
+ 8 decomposes into 3+[5] and we know that 5 can be further decomposed into 3+2
+ Furthermore the product of [5]=3x2=6 and the product of [8]=3x3x2 which is the same as 3x6

We can then have an array that stores the previously decomposed values, so that when obtaining a new one
we can check a previous one an dmultiply it by 3.
