# **EX 1B Power of 2**

## **DATE: 10-08-2025**

## **AIM:**

To write a Java program that checks whether a given integer **n** is a power of two.
An integer **n** is a power of two if there exists an integer **x** such that:
**n = 2ˣ**.

---

## **Algorithm**

1. Start the program.
2. Read the integer value **n** from the user.
3. If **n ≤ 0**, return false (because powers of 2 are always positive).
4. Use a loop to check whether **n** becomes 1 when repeatedly divided by 2.
5. If n becomes 1, display **true**; otherwise display **false**.

---

## **Program:**

```JAVA
/*
Program to check if a number is a Power of 2
Developed by: MADHAN BABU P
Register Number: 212222230075
*/
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        boolean result = true;
        
        if(n <= 0)
            result = false;
        else{
            while(n > 1){
                if(n % 2 != 0){
                    result = false;
                    break;
                }
                n = n / 2;
            }
        }
        
        System.out.println(result);
    }
}
```

---

## **Output:**

<img width="1264" height="242" alt="image" src="https://github.com/user-attachments/assets/9ead7ad4-b02e-405e-9e35-b2f149fa3e67" />

---

## **Result:**

The program was successfully implemented and the expected output was verified.

---
