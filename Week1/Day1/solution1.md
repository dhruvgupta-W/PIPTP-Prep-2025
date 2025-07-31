Pseudocode:
1. Integer funn(Integer a, Integer b)
2.     if(a > 0)
3.         return funn(a - 2, a + b) + funn(a - 3, a + b) + funn(a - 4, a + b)
4.     Else
5.         a = b
6.         b = a
7.         return a + b
8.     End if
9. End function
Goal:
Find funn(4, 3)

Step-by-step recursion:
We compute:

funn(4, 3) = funn(2, 7) + funn(1, 7) + funn(0, 7)

funn(2, 7) = funn(0, 9) + funn(-1, 9) + funn(-2, 9)

funn(0, 9) → a = b = 9 → return 18

funn(-1, 9) → a = b = 9 → return 18

funn(-2, 9) → a = b = 9 → return 18

So total = 18 + 18 + 18 = 54

funn(1, 7) = funn(-1, 8) + funn(-2, 8) + funn(-3, 8)

Each gives 16 (a = b = 8 → return 16)

Total = 16 + 16 + 16 = 48

funn(0, 7) → a = b = 7 → return 14

Final Result:
Copy
Edit
funn(4, 3) = 54 + 48 + 14 = 116
