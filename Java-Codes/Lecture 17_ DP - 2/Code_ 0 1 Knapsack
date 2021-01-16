// Code: 0 1 Knapsack
// Send Feedback
// A thief robbing a store and can carry a maximal weight of W into his knapsack. There are N items and ith item weigh wi and is value vi. What is the maximum value V, that thief can take ?
// Input Format :
// Line 1 : N i.e. number of items
// Line 2 : N Integers i.e. weights of items separated by space
// Line 3 : N Integers i.e. values of items separated by space
// Line 4 : Integer W i.e. maximum weight thief can carry
// Output Format :
// Line 1 : Maximum value V
// Constraints
// 1 <= N <= 20
// 1<= wi <= 100
// 1 <= vi <= 100
// Sample Input 1 :
// 4
// 1 2 4 5
// 5 4 8 6
// 5
// Sample Output :
// 13

public class Solution {
	
	public static int knapsack(int[] weight,int value[],int maxWeight, int n){
 if (n == 0 || maxWeight == 0) {
            return 0;
        }

        int v1 = 0, v2 = 0, result = 0;
        int[] tw = new int[n - 1];
        int[] tv = new int[n - 1];
        for (int i = 0; i < n - 1; i++) {
            tw[i] = weight[i + 1];
            tv[i] = value[i + 1];
        }
        if (weight[0] <= maxWeight) {
            v1 = value[0];
            v1 = v1 + knapsack(tw, tv, maxWeight - weight[0], n - 1);
            v2 = 0;
            v2 = v2 + knapsack(tw, tv, maxWeight, n - 1);
            result = Math.max(v1, v2);
        } else {
            result = result + knapsack(tw, tv, maxWeight, n - 1);
        }
        return result;
    }
}
