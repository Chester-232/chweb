+++
date = '2025-03-31T22:24:23+08:00'
draft = true
title = 'Divisibility and number theory'
summary = "A comprehensive guide on divisibility rules, prime and composite numbers, GCD, and LCM, with manual number conversions using the Euclidean method for number system representation."
tags = [ "Discrete Mathematics" ]
[params]
math = true
+++

## Number Theory (A.K.A. Higher Arithmetic)

A branch of mathematics concerned with the properties of integers.

---

## Divisibility

Divisibility means dividing one number evenly by another, without leaving a remainder.

- $d \mid n$ means that $d$ divides $n$
- $d \nmid n$ means that $d$ does not divide $n$
- Conditions:
  - $d \neq 0$
  - $n \neq 0$
  - If $d \times q = n$, then $q = \frac{n}{d}$

---

## Divisibility Rules

### Rule for 2
A number is divisible by 2 if its **last digit** is even (i.e. 0, 2, 4, 6, or 8).

**Examples:**

- $2 \mid 128$ → 8 is even ⇒ ✅
- $2 \nmid 129$ → 9 is odd ⇒ ❌

---

### Rule for 3
A number is divisible by 3 if the **sum of its digits** is divisible by 3.

**Examples:**

- $3 \mid 381$:  
  $3 + 8 + 1 = 12$ → $3 \mid 12$ ⇒ ✅  
- $3 \nmid 217$:  
  $2 + 1 + 7 = 10$ → $3 \nmid 10$ ⇒ ❌

---

### Rule for 4
A number is divisible by 4 if the **last two digits** form a number divisible by 4.

**Examples:**

- $4 \mid 1312$:  
  Last two digits: 12 → $4 \mid 12$ ⇒ ✅  
- $4 \nmid 7019$:  
  Last two digits: 19 → $4 \nmid 19$ ⇒ ❌

---

### Rule for 5
A number is divisible by 5 if its **last digit** is either 0 or 5.

**Examples:**

- $5 \mid 205$ → Last digit is 5 ⇒ ✅  
- $5 \nmid 128$ → Last digit is 8 ⇒ ❌

---

### Rule for 6
A number is divisible by 6 if it is divisible by **both 2 and 3**.

**Examples:**

- $6 \mid 114$:  
  - Divisible by 2: last digit 4 is even ⇒ ✅  
  - Divisible by 3: $1 + 1 + 4 = 6$ → $3 \mid 6$ ⇒ ✅  
- $6 \nmid 308$:  
  - Divisible by 2: 8 is even ⇒ ✅  
  - Not divisible by 3: $3 + 0 + 8 = 11$ ⇒ ❌

---

### Rule for 7
Take the last digit, double it, and subtract it from the rest of the number. If the result is divisible by 7, then the number is divisible by 7.

**Examples:**

- $7 \mid 672$:  
  $67 - 2 \times 2 = 63$ → $7 \mid 63$ ⇒ ✅  
- $7 \nmid 905$:  
  $90 - 2 \times 5 = 80$ → $7 \nmid 80$ ⇒ ❌

---

### Rule for 8
A number is divisible by 8 if the **last three digits** form a number divisible by 8.

**Examples:**

- $8 \mid 109816$:  
  Last three digits: 816 → $8 \mid 816$ ⇒ ✅  
- $8 \nmid 216302$:  
  Last three digits: 302 → $8 \nmid 302$ ⇒ ❌

---

### Rule for 9
A number is divisible by 9 if the **sum of its digits** is divisible by 9.

**Example:**

- $9 \mid 1629$:  
  $1 + 6 + 2 + 9 = 18$ → $9 \mid 18$ ⇒ ✅

---

### Rule for 10
A number is divisible by 10 if it ends in **0**.

**Examples:**

- $10 \mid 130$ → ends in 0 ⇒ ✅  
- $10 \nmid 131$ → ends in 1 ⇒ ❌

---

### Rule for 11
A number is divisible by 11 if the **alternating sum of its digits** (i.e., subtracting every other digit) is divisible by 11 or equals 0.

**Examples:**

- $11 \mid 3729$:  
  $(3 + 2) - (7 + 9) = 5 - 16 = -11$ ⇒ $11 \mid 11$ ⇒ ✅  
- $11 \nmid 987$:  
  $(9 + 7) - 8 = 16 - 8 = 8$ ⇒ $11 \nmid 8$ ⇒ ❌

---

### Rule for 12
A number is divisible by 12 if it is divisible by **both 3 and 4**.

**Examples:**

- $12 \mid 648$:  
  - $6 + 4 + 8 = 18$ ⇒ $3 \mid 18$  
  - Last two digits: 48 ⇒ $4 \mid 48$  
  ⇒ ✅  
- $12 \nmid 524$:  
  - $5 + 2 + 4 = 11$ ⇒ $3 \nmid 11$  
  ⇒ ❌

---

## Prime Numbers

These are **positive integers greater than 1** that are only divisible by **1 and themselves**.

**Examples:** 2, 3, 5, 7, 11, 13, ...

---

## Composite Numbers

Composite numbers are **positive integers greater than 1** that are **not prime**.  
They have more than two distinct positive divisors.

**Examples:**

- 4 → $2 \times 2$
- 9 → $3 \times 3$
- 12 → $2 \times 2 \times 3$

---

## Greatest Common Divisor (GCD)

The **GCD** of two or more integers is the largest positive integer that divides each of the numbers.

- Denoted as $\gcd(a, b)$
- Can be found using **prime factorization** or the **Euclidean algorithm**

### Example: GCD of 375 and 525

**Prime factorization method:**

- 375 = $3 \times 5^3$
- 525 = $3 \times 5^2 \times 7$

**Common factors:** $3 \times 5^2 = 75$  
⇒ $\gcd(375, 525) = 75$

---

## Least Common Multiple (LCM)

The **LCM** of two or more integers is the smallest number that is a multiple of all the given numbers.

- Denoted as $\text{lcm}(a, b)$
- Often found using prime factorization or the formula:  
  $\text{lcm}(a, b) = \frac{a \times b}{\gcd(a, b)}$

**Example:**

### LCM of 12 and 18

- $\gcd(12, 18) = 6$  
- $\text{lcm}(12, 18) = \frac{12 \times 18}{6} = 36$

---

## Number Systems

### Decimal (Base 10)
Digits: 0–9  
Example: `123`, `45`

### Binary (Base 2)
Digits: 0, 1  
Prefix: `0b` or `0x` in some notations  
Example: `0b1010` (10 in decimal)

### Octal (Base 8)
Digits: 0–7  
Prefix: `0o`  
Example: `0o17` (15 in decimal)

### Hexadecimal (Base 16)
Digits: 0–9 and A–F (A=10, B=11, ..., F=15)  
Prefix: `0x`  
Example: `0x1F` (31 in decimal)

---

## Conversion Between Number Systems Using the Euclidean Method

The Euclidean algorithm is used for converting between different bases manually. Below is the step-by-step process of converting a decimal number to any base using the Euclidean method.

### Example 1: Convert 156 to Binary (Base 2)

1. Divide 156 by 2:  
   156 ÷ 2 = 78 remainder 0
2. Divide 78 by 2:  
   78 ÷ 2 = 39 remainder 0
3. Divide 39 by 2:  
   39 ÷ 2 = 19 remainder 1
4. Divide 19 by 2:  
   19 ÷ 2 = 9 remainder 1
5. Divide 9 by 2:  
   9 ÷ 2 = 4 remainder 1
6. Divide 4 by 2:  
   4 ÷ 2 = 2 remainder 0
7. Divide 2 by 2:  
   2 ÷ 2 = 1 remainder 0
8. Divide 1 by 2:  
   1 ÷ 2 = 0 remainder 1

Now, read the remainders from bottom to top:  
$156_{10} = 10011100_2$

### Example 2: Convert 156 to Hexadecimal (Base 16)

1. Divide 156 by 16:  
   156 ÷ 16 = 9 remainder 12 (12 in hexadecimal is C)
2. Divide 9 by 16:  
   9 ÷ 16 = 0 remainder 9

Now, read the remainders from bottom to top:  
$156_{10} = 9C_{16}$

This method can be applied to convert between any number systems by following similar steps for division and taking remainders.

---
