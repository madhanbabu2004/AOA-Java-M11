# **EX 1D Sorted Array using Divide and Conquer Approach**

## **DATE: 28-08-2025**

## **AIM:**

To write a Java program that finds the median of two sorted arrays **nums1** and **nums2** of sizes **m** and **n** respectively.
The overall time complexity should be **O(log(m + n))**.

---

## **Algorithm**

1. Start the program.
2. Read the sizes of the two arrays and their elements.
3. Use two pointers to pick the smallest element from both arrays step-by-step.
4. Traverse until reaching the median index (middle of combined sorted list).
5. If the total number of elements is odd, return the middle element; otherwise return the average of the two middle elements.

---

## **Program:**

```JAVA
/*
Program to find median of two sorted arrays using Divide and Conquer
Developed by: MADHAN BABU P 
Register Number: 212222230075
*/
import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;

    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1;
    }

    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int total = nums1.length + nums2.length;
        int mid1 = (total - 1) / 2;
        int mid2 = total / 2;
        int val = -1, prev = -1;

        for (int i = 0; i <= mid2; i++) {
            prev = val;
            val = getMin(nums1, nums2);
        }

        if (total % 2 == 1) {
            return val;
        } else {
            return (prev + val) / 2.0;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}
```

---

## **Output:**

<img width="1223" height="381" alt="image" src="https://github.com/user-attachments/assets/deef150d-40fc-4ad2-bb9c-2b5c167128ab" />

---

## **Result:**

The program was successfully implemented and the expected output was verified.

---
