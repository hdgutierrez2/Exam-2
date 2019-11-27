Looking for a palindrome we can easily find them suing the comparing method, the first character must equal the last character,
the next character must equal the nest to the last and so on.

Except with odd number of letters palindromes where the sustring inside of it must also be a palindrome.

We then know that for each subsequent palindrome the substring inside of it must also be a palindrome.

Example:

The string "abba" is palindrome since the inner string "bb" is also palindrome and "a"="a".

Following this we have 4 rules:
+ Every substring of length 1 is always a palindrome
+ Every substring of length 2 is a palindrome if they equal to one another.
+ Every substring of length 3 is a palindrome if the characters on the left and right are equal.
+ Every substring of length 4 or more are only a palindrome if the substring inside of it is a palindrome and if the character on the left and right are the same.

If we are constantly checking if a letter is the same to another we this can be represented in a grid as follows: 
                  
                  A B C 
                A    
                B    
                C  
 
We can then fill the while grid following the previous constrains. 
 
                  A B C 
                A T F F 
                B   T F 
                C     T 
                
To fill the grid we are constantly cheking if the characters are equal to the other one but also when
encountering characters of length 4 or greater we are cheking the previous cell.

If the characters on both ends are equal but the previous cell is false, then it means that there is no
inner palindrome, saving us the time of checking again and again the inner substring of each substring.
