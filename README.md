# 🔁 Types of Recursion: Head Recursion in Python

## 🎯 AIM:
To write a Python program to demonstrate **Head Recursion** by finding and printing the sequence based on the sum of all digits (even or odd adjusted input).

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `fun(n)`
3. In the function:
   - Create a recursive call at the **beginning** (Head Recursion)
   - Print the result after the recursive call
4. Take input from the user
5. If input is odd, convert it to the next even number
6. Call the recursive function
7. **Stop**

## 💻 PROGRAM:
```
def sum_of_digits(n):
    """Return the sum of digits of a number"""
    return sum(int(digit) for digit in str(n))

def head_recursive_sequence(n):
    if n <= 0:
        return
   
    sum_digits = sum_of_digits(n)
    if sum_digits % 2 == 0:
        head_recursive_sequence(n - 2)
    else:
        head_recursive_sequence(n - 1)
    print(n, end=' ')

number = 10
print(f"Head Recursion Sequence starting from {number}:")
head_recursive_sequence(number)
```
## OUTPUT:
```
Input           Result

 10           Head Recursion Sequence starting from 10:
              1 2 3 4 6 8 10
```
## RESULT:
The program was successful.

# 🔁 Recursion:Palindrome Checker Using Recursion in Python

## 🎯 AIM:
To write a Python program to check whether a given string is a **palindrome** using **recursion**.

---

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `is_palindrome(word)`
   - **Base Case:** If the string length is less than 1, return `True`
   - **Recursive Case:** If the first and last characters match, call the function recursively on the substring without first and last characters
   - Else, return `False`
3. Get input from the user
4. Call the recursive function
5. Print whether the string is a palindrome
6. **Stop**

---

## 💻 PROGRAM:
```
def sum_of_digits(n):
    return sum(int(d) for d in str(n))

def head_recursion(n):
    if n == 0:
        return
    head_recursion(n - 1) 
    print(n, end=' ')

num = 123
digit_sum = sum_of_digits(num)

if digit_sum % 2 == 0:
    adjusted = num + 2
else:
    adjusted = num + 3

print(f"Sum of digits of {num} is {digit_sum}")
print("Printing sequence using head recursion up to adjusted value:")
head_recursion(5)  
```
## OUTPUT:
```
'madam' is a palindrome:
'hello' is not a palindrome.
'racecar' is a palindrome:
```
## RESULT:
The program was successful.

# # 🔁 Recursion:Sum of Digits using Recursion in Python

## 🎯 AIM:
To write a Python program to calculate the **sum of all digits** in a number using **recursion**.

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `sum_digit(n)` that:
   - Returns 0 if `n <= 0` (Base Case)
   - Else, returns `n % 10 + sum_digit(n // 10)` (Recursive Case)
3. Take integer input from the user.
4. Call the recursive function and store the result.
5. Print the result.
6. **Stop**

## 💻 PROGRAM:
```
def sum_of_digits(n):
 
    if n == 0:
        return 0
    else:
        return n % 10 + sum_of_digits(n // 10)

num = 12345
result = sum_of_digits(num)

print(f"The sum of the digits of {num} is {result}")
```
## OUTPUT:
```
Input          Result
12345        The sum of the digits of 12345 is 15
```
## RESULT:
The program was successful.

# 📐 Taylor Series Using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate a **Taylor Series** using **recursion**, where values of `x` and `n` are taken from the user.

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `x` and `n`
3. Get values for `x` and `n` from the user
4. Define a recursive function `series(x, n)`
   - **Base case:** If `n == 0`, return 1
   - **Recursive case:** Return `x**n / n + series(x, n-1)`
5. Print the result
6. **Stop**

## 💻 PROGRAM:
```
def taylor_series(x, n, current_term=0):

    if n == 0:
        return 1
 
    else:
        return (x ** current_term) / factorial(current_term) + taylor_series(x, n-1, current_term + 1)

def factorial(num):
    # Recursive function to calculate factorial
    if num == 0:
        return 1
    else:
        return num * factorial(num - 1)
x = float(input("Enter the value of x: "))
n = int(input("Enter the number of terms in the Taylor Series: "))

result = taylor_series(x, n)

print(f"The value of e^{x} using Taylor Series with {n} terms is: {result}")

```

## OUTPUT:
```
Input         Result
  1        Enter the number of terms in the Taylor Series: 10
```
## RESULT:
The program was successful.

# 📐 Taylor Series:sinh(x) Evaluation using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate the value of **sinh(x)** for **n terms** using recursion.

---

## 🧠 ALGORITHM:

1. **Start**
2. Read input for variable `x` (angle or number)
3. Read input for variable `n` (number of terms)
4. Define a function `fact(n)`:
   - If `n <= 1`, return 1
   - Else, return `n * fact(n - 1)` (recursive factorial)
5. Define a function `sinh(x, n)`:
   - If `n == 0`, return `x`
   - Else, return `(pow(x, 2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)`
6. Call the `sinh(x, n)` function and print the result
7. **Stop**

---

## 💻 PROGRAM:
```
def sinh(x, n, current_term=0):
 
    if n == 0:
        return 0
    else:
        term = (x ** (2*current_term + 1)) / factorial(2 * current_term + 1)
        return term + sinh(x, n-1, current_term + 1)
def factorial(num):
    if num == 0:
        return 1
    else:
        return num * factorial(num - 1)

x = float(input())
n = int(input())
result = sinh(x, n)

print(f"The value of sinh({x}) using Taylor Series with {n} terms is: {result}")
````
## OUTPUT:
```
Input         Result
  1       Enter the number of terms in the Taylor Series: 10
```
## RESULT:
The program was successful
