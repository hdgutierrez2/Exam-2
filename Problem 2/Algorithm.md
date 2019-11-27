class Solution {

    public int countSubstrings(String s) {
    
    	int n = s.length();
      
    	int count = 0;
	    
      boolean[][] dp = new boolean[n][n];
    	
      for (int i=0; i<n; i++){
      
        dp[i][i] = true; // Substrings of length 1 will always be true, add 1 to count for each one
      	
          count++;
  	  }
  	
      for (int i=1; i<n; i++){
   		  
        dp[i-1][i] = s.charAt(i-1) == s.charAt(i);
   		  
        if (dp[i-1][i]){ //Susbtring of lenght 2 are only true if two characters beside each other are equal
			    
          count++;
		    
        }
  	
      }
  	
      for (int i=2; i<n; i++){
   		
        for (int j=0; j<n-i; j++){
         
            dp[j][j+i] = s.charAt(j) == s.charAt(j+i) && dp[j+1][j+i-1];
            
                if (dp[j][j+i]){ //Substrings of length 3 or more are only true if two characters on the ends are equal and the inner palindrome is true
				
                    count++;
			
              }
      		
          }
          
    	}
                
	    return count;
    
    }

}
