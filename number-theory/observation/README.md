1)

---

```
157 = 13^2 - 13 + 1
13 = 4^2 - 4 + 1
Therefore: 157 = (4^2 - 4 + 1)^2 - (4^2 - 4 + 1) + 1

104 = 5^3 - 5^2 + 5 - 1
5 = 2^3 - 2^2 + 2 - 1
Therefore: 104 = (2^3 - 2^2 + 2 - 1)^3 - (2^3 - 2^2 + 2 - 1)^2 + (2^3 - 2^2 + 2 - 1) - 1

13421 = 11^4 - 11^3 + 11^2 - 11 + 1
11 = 2^4 - 2^3 + 2^2 - 2 + 1
Therefore: 13421 = (2^4 - 2^3 + 2^2 - 2 + 1)^4 - (2^4 - 2^3 + 2^2 - 2 + 1)^3 + (2^4 - 2^3 + 2^2 - 2 + 1)^2 - (2^4 - 2^3 + 2^2 - 2 + 1) + 1

157 is the only 3-digit number with this property where each step uses n^2 - n + 1 and digit sums.
```

2)

# Infinite Series Whose Coefficients Are the Digits of 7^k

This series has the decimal digits of every power \( 7^k \) (for \( k = 0, 1, 2, \dots \)) as its coefficients, in order.

---

## Expanded Series (first 9 powers shown)

\[
\begin{aligned}
S(x) = 
& 1 \\
& + 7 x^{1} \\
& + 4 x^{2} + 9 x^{3} \\
& + 3 x^{4} + 4 x^{5} + 3 x^{6} \\
& + 2 x^{7} + 4 x^{8} + 0 x^{9} + 1 x^{10} \\
& + 1 x^{11} + 6 x^{12} + 8 x^{13} + 0 x^{14} + 7 x^{15} \\
& + 1 x^{16} + 1 x^{17} + 7 x^{18} + 6 x^{19} + 4 x^{20} + 9 x^{21} \\
& + 8 x^{22} + 2 x^{23} + 3 x^{24} + 5 x^{25} + 4 x^{26} + 3 x^{27} \\
& + 5 x^{28} + 7 x^{29} + 6 x^{30} + 4 x^{31} + 8 x^{32} + 0 x^{33} + 1 x^{34} \\
& + 4 x^{35} + 0 x^{36} + 3 x^{37} + 5 x^{38} + 3 x^{39} + 6 x^{40} + 0 x^{41} + 7 x^{42} \\
& + \dots
\end{aligned}
\]

---

## Mapping of Powers to Digits

| \( k \) | \( 7^k \)   | Digits (coefficients)        | Exponent range |
|---------|-------------|------------------------------|----------------|
| 0       | 1           | 1                            | 0              |
| 1       | 7           | 7                            | 1              |
| 2       | 49          | 4, 9                         | 2–3            |
| 3       | 343         | 3, 4, 3                      | 4–6            |
| 4       | 2401        | 2, 4, 0, 1                   | 7–10           |
| 5       | 16807       | 1, 6, 8, 0, 7                | 11–15          |
| 6       | 117649      | 1, 1, 7, 6, 4, 9             | 16–21          |
| 7       | 823543      | 8, 2, 3, 5, 4, 3             | 22–27          |
| 8       | 5764801     | 5, 7, 6, 4, 8, 0, 1          | 28–34          |
| 9       | 40353607    | 4, 0, 3, 5, 3, 6, 0, 7       | 35–42          |
| 10      | 282475249   | 2, 8, 2, 4, 7, 5, 2, 4, 9    | 43–51          |
| ...     | ...         | ...                          | ...            |

---

## Closed Form

\[
S(x) = \sum_{k=0}^{\infty} \sum_{j=0}^{D_k - 1} d_{k,j} \, x^{L(k) + (D_k - 1 - j)}
\]

where:
- \( D_k = \lfloor k \log_{10} 7 \rfloor + 1 \) is the number of digits of \( 7^k \),
- \( d_{k,j} \) is the \( j \)-th digit of \( 7^k \) (from most significant, \( j=0 \)),
- \( L(k) = \sum_{i=0}^{k-1} D_i \) is the total digits before power \( k \).

Evaluating at \( x = 1/10 \) gives the real number:
\[
S(1/10) = 0.1\,7\,49\,343\,2401\,16807\,117649\,\dots
\]
whose decimal expansion is the concatenation of all powers of 7.

---
