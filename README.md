Remove Duplicates
Difficulty: EasyAccuracy: 52.35%Submissions: 132K+Points: 2
Given a string str without spaces, the task is to remove all duplicate characters from it, keeping only the first occurrence.

Note: The original order of characters must be kept the same. 

Examples :

Input: str = "zvvo"
Output: "zvo"
Explanation: Only keep the first occurrence
Input: str = "gfg"
Output: "gf"
Explanation: Only keep the first occurrence
Expected Time Complexity: O(n)
Expected Auxiliary Space: O(1)

Constraints:
1 <= |str| <= 105
str contains lowercase English alphabets


//{ Driver Code Starts
// Initial Template for Java

import java.io.*;
import java.util.*;

class GFG {
    public static void main(String args[]) throws IOException {
        BufferedReader read = new BufferedReader(new InputStreamReader(System.in));
        int t = Integer.parseInt(read.readLine());
        while (t-- > 0) {
            String s = read.readLine();

            Solution ob = new Solution();
            String result = ob.removeDups(s);

            System.out.println(result);
        }
    }
}
// } Driver Code Ends


// User function Template for Java

class Solution {
    String removeDups(String str) {
        // code here
          Map<Character, Integer> map = new HashMap<>();
        StringBuilder rt= new StringBuilder();
        for(int i=0;i<str.length();i++){
            Character ch= str.charAt(i);
            
          if(!(map.containsKey(ch)))
          {
              
              
              map.put(ch,1);
              rt.append(ch);
              
          }
        }
        return rt.toString();
              
    }
}
