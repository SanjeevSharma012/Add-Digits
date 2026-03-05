➕ Add Digits (Digital Root)
📌 Problem Statement

Given an integer num, repeatedly add all its digits until the result has only one digit, and return it.

📝 Example
Input:  num = 38
Output: 2

Explanation:
3 + 8 = 11  
1 + 1 = 2
💡 Approach Used (Iterative Method)

We:

Keep summing digits while the number has more than one digit (num >= 10).

Extract digits using:

num % 10 → last digit

num /= 10 → remove last digit

Store digit sum and repeat until a single digit remains.

🚀 Java Implementation
class Solution {
    public int addDigits(int num) {

        while (num >= 10) {
            int sum = 0;

            while (num > 0) {
                int r = num % 10;
                sum += r;
                num /= 10;
            }

            num = sum;
        }

        return num;
    }
}
⏱ Time Complexity

O(d × k)

d = number of digits

k = number of times we repeat the process

In worst case, it runs a few times only.

💾 Space Complexity

O(1) (No extra space used)
