We basically want to find the path with the minimum sum going from the top row to the bottom row, given
a column constrain

First we are going to need a new 2d array, with the same dimensions as the 2d "A" array we start with
+ int n = A.length;
+ int[][] dp = new int[n][n];

We need to initialize our first row of the new array with the same values from "A" since we are going to
proceed from those values.
+ dp[0] = A[0];

Another thing to note is that when getting to anyone of the cells in the next row inly has 3 different paths 
that we can use to reach it, excluding the "dp[i][0]" and the "dp[i][A.length-1]" which only have 2 paths.

Transverse the whole 2d "A" array adding the minimum from the 3 or 3 values to the corresponding cells bellow
it.
