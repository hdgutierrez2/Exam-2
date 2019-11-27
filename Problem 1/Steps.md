Step 1: Small 
  + [2,3,5,5] --> Alex can win, return true
  + [2,5,1,3] --> Alex can win

Step 2: Solve
  + No matter the way we arrange the pile of stone , Alex will always win
  + Since Alex takes the first pile initialy, she can choose which pile to take as second and so on
  + No matter how the piles are arranged Alex can always take the pile with the largest amount of rocks

Step 3: Find Patterm
  + Since Alex will always win we can just return true
 
Step 4: Code
  + Return true
