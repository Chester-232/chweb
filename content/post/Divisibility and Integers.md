+++
date = '2025-03-31T22:24:23+08:00'
draft = false
title = 'Divisibility and Number Theory: A Beginner’s Guide'
summary = "Learn the basics of divisibility rules, prime and composite numbers, GCD, LCM, and how to convert numbers between different systems using simple methods."
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

**Euclidean algorithm method:**

Formula: $a = bq + r$

where  
- $q$ is the quotient (the largest integer such that $bq \le a$),  
- $r = a - bq$ is the remainder.  


1. $525 = 375(1) + 150$
2. $375 = 150(2) + 75$
3. $150 = 75(2) + 0$  

When the remainder is zero, the last nonzero remainder is the GCD:

$$
\gcd(375, 525) = 75
$$


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

Here’s how to convert between different number systems using the Euclidean method. I'll give examples for converting **Decimal to Binary**, **Decimal to Octal**, **Decimal to Hexadecimal**, and **Binary to Decimal**:


## Number Systems Conversion Using the Euclidean Method

### 1. **Decimal to Binary (Base 2)**
To convert a decimal number to binary, repeatedly divide the number by 2 and record the remainders. The binary number is the sequence of remainders read from bottom to top.

**Example 1: Decimal 13 to Binary**

- 13 ÷ 2 = 6, remainder 1
- 6 ÷ 2 = 3, remainder 0
- 3 ÷ 2 = 1, remainder 1
- 1 ÷ 2 = 0, remainder 1

Binary: **1101**

---

**Example 2: Decimal 25 to Binary**

- 25 ÷ 2 = 12, remainder 1
- 12 ÷ 2 = 6, remainder 0
- 6 ÷ 2 = 3, remainder 0
- 3 ÷ 2 = 1, remainder 1
- 1 ÷ 2 = 0, remainder 1

Binary: **11001**

---

**Example 3: Decimal 56 to Binary**

- 56 ÷ 2 = 28, remainder 0
- 28 ÷ 2 = 14, remainder 0
- 14 ÷ 2 = 7, remainder 0
- 7 ÷ 2 = 3, remainder 1
- 3 ÷ 2 = 1, remainder 1
- 1 ÷ 2 = 0, remainder 1

Binary: **111000**

---

**Example 4: Decimal 7 to Binary**

- 7 ÷ 2 = 3, remainder 1
- 3 ÷ 2 = 1, remainder 1
- 1 ÷ 2 = 0, remainder 1

Binary: **111**

---

### 2. **Decimal to Octal (Base 8)**
To convert a decimal number to octal, divide the number by 8 and record the remainders. The octal number is the sequence of remainders read from bottom to top.

**Example 1: Decimal 65 to Octal**

- 65 ÷ 8 = 8, remainder 1
- 8 ÷ 8 = 1, remainder 0
- 1 ÷ 8 = 0, remainder 1

Octal: **101**

---

**Example 2: Decimal 128 to Octal**

- 128 ÷ 8 = 16, remainder 0
- 16 ÷ 8 = 2, remainder 0
- 2 ÷ 8 = 0, remainder 2

Octal: **200**

---

**Example 3: Decimal 255 to Octal**

- 255 ÷ 8 = 31, remainder 7
- 31 ÷ 8 = 3, remainder 7
- 3 ÷ 8 = 0, remainder 3

Octal: **377**

---

**Example 4: Decimal 43 to Octal**

- 43 ÷ 8 = 5, remainder 3
- 5 ÷ 8 = 0, remainder 5

Octal: **53**

---

### 3. **Decimal to Hexadecimal (Base 16)**
To convert a decimal number to hexadecimal, divide the number by 16 and record the remainders. The hexadecimal number is the sequence of remainders read from bottom to top.

**Example 1: Decimal 34 to Hexadecimal**

- 34 ÷ 16 = 2, remainder 2
- 2 ÷ 16 = 0, remainder 2

Hexadecimal: **22**

---

**Example 2: Decimal 255 to Hexadecimal**

- 255 ÷ 16 = 15, remainder 15 (F)
- 15 ÷ 16 = 0, remainder 15 (F)

Hexadecimal: **FF**

---

**Example 3: Decimal 501 to Hexadecimal**

- 501 ÷ 16 = 31, remainder 5
- 31 ÷ 16 = 1, remainder 15 (F)
- 1 ÷ 16 = 0, remainder 1

Hexadecimal: **1F5**

---

**Example 4: Decimal 56 to Hexadecimal**

- 56 ÷ 16 = 3, remainder 8
- 3 ÷ 16 = 0, remainder 3

Hexadecimal: **38**

---

### 4. **Binary to Decimal (Base 10)**
To convert a binary number to decimal, multiply each binary digit by the corresponding power of 2, starting from the rightmost digit (least significant bit). Sum the results.

**Example 1: Binary 1101 to Decimal**

- $(1 \times 2^3) + (1 \times 2^2) + (0 \times 2^1) + (1 \times 2^0)$  
- $8 + 4 + 0 + 1 = 13$

Decimal: **13**

---

**Example 2: Binary 10101 to Decimal**

- $(1 \times 2^4) + (0 \times 2^3) + (1 \times 2^2) + (0 \times 2^1) + (1 \times 2^0)$  
- $16 + 0 + 4 + 0 + 1 = 21$

Decimal: **21**

---

**Example 3: Binary 111000 to Decimal**

- $(1 \times 2^5) + (1 \times 2^4) + (1 \times 2^3) + (0 \times 2^2) + (0 \times 2^1) + (0 \times 2^0)$  
- $32 + 16 + 8 + 0 + 0 + 0 = 56$

Decimal: **56**

---

**Example 4: Binary 1111 to Decimal**

- $(1 \times 2^3) + (1 \times 2^2) + (1 \times 2^1) + (1 \times 2^0)$  
- $8 + 4 + 2 + 1 = 15$

Decimal: **15**

---

These examples demonstrate how the Euclidean method works for converting numbers between different systems! Let me know if you need more details or examples.
