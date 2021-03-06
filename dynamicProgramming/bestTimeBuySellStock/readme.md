# Best time to buy and sell stock

## Problem Definition
Say you have an array for which the ith element is the price of a given stock on day i.

If you were only permitted to complete at most one transaction (i.e., buy one and sell one share of the stock), design an algorithm to find the maximum profit.

Note that you cannot sell a stock before you buy one.

Example 1:

Input: [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
             Not 7-1 = 6, as selling price needs to be larger than buying price.

Example 2:

Input: [7,6,4,3,1]
Output: 0
Explanation: In this case, no transaction is done, i.e. max profit = 0.

## Questions to ask
- Is this just tracking one stock over time?
- What should we do if the array is empty?

## Complexity Analysis
The implementation runs in linear time O(n) and constant space O(1).
Basically we start out with a specific min and potential diff (the first array index and the second index minus the first index respectively).
At each point in the for loop, we add the max of each potential diff vs the first diff (maxDiff) and find the minimum between the minimum index and the next index in the array.
We use the minimum because we want to buy at the lowest cost we can.
