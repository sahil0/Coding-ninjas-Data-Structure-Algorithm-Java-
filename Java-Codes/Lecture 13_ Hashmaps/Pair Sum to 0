// Pair Sum to 0
// Send Feedback
// Given a random integer array A of size N. Find and print the pair of elements in the array which sum to 0.
// Array A can contain duplicate elements.
// While printing a pair, print the smaller element first.
// That is, if a valid pair is (6, -6) print "-6 6". There is no constraint that out of 5 pairs which have to be printed in 1st line. You can print pairs in any order, just be careful about the order of elements in a pair.
// Input format :
// Line 1 : Integer N (Array size)
// Line 2 : Array elements (separated by space)
// Output format :
// Line 1 : Pair 1 elements (separated by space)
// Line 2 : Pair 2 elements (separated by space)
// Line 3 : and so on
// Constraints :
// 0 <= N <= 10^4
// Sample Input:
// 5
// 2 1 -2 2 3
// Sample Output :
// -2 2
// -2 2


import java.util.*;

public class Solution {
	public static void PairSum(int[] input, int size) {
		
		/* Your class should be named Solution
		 * Don't write main().
		 * Don't read input, it is passed as function argument.
		 * Print the desired output and don't return anything.
	 	 * Taking input is handled automatically.
		 */
        
  Map<Integer, Integer> map = new HashMap<>();
    for (int element : input) {
      if (map.containsKey(element)) {
        map.put(element, map.get(element) + 1);
      } else {
        map.put(element, 1);
      }
    }

    for (int element : input) 
    {
      // Check for its pair and get frequency
      int pairElement = -1 * element;
      if (map.containsKey(pairElement))
      {
        int freq = map.get(pairElement);
        if (map.containsKey(element))
        {
          freq *= map.get(element);
        }
        map.put(element, 0);
        map.put(pairElement, 0);
        while (freq-- > 0) {
          System.out.println(element < (-1 * element) ? element + " " + (-1 * element) : (-1 * element) + " " + element);
        }
      }
    
    }
        
        
        
  }
}
