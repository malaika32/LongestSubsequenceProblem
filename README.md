# LongestSubsequenceProblem

A longest common subsequence (LCS) is defined as the longest subsequence which is common in all given input sequences.
Follow the below steps to implement the idea:

Create a recursive function LCREcursion and LCHelper.
Check the relation between the First characters of the strings that are not yet processed.
Depending on the relation call the next recursive function as mentioned above.
Return the length of the LCS received as the answer.

We can use the following steps to implement the dynamic programming approach for LCS.

Create a 2D array dp[][] with rows and columns equal to the length of each input string plus 1 [the number of rows indicates the indices of S1 and the columns indicate the indices of S2].
Initialize the first row and column of the dp array to 0.
Iterate through the rows of the dp array, starting from 1 (say using iterator i).
For each i, iterate all the columns from j = 1 to n:
If S1[i-1] is equal to S2[j-1], set the current element of the dp array to the value of the element to (dp[i-1][j-1] + 1).
Else, set the current element of the dp array to the maximum value of dp[i-1][j] and dp[i][j-1].
After the nested loops, the last element of the dp array will contain the length of the LCS.
