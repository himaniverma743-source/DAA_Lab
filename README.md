<div align="center">
MODY UNIVERSITY OF SCIENCE AND TECHNOLOGY
School of Engineering and Technology
<br>
<img width="154" height="157" alt="Mody\_University\_logo" src="https://github.com/user-attachments/assets/11e32514-7869-4f2d-afc9-b45171b58488" />

<br>
PYTHON PROGRAMMING LAB
LAB RECORD
<br><br>
Student Name: Himani
Enrollment Number: 240044
<br>
Faculty Name: Dr. P. K. Bishnoi
<br><br>
Mody University of Science and Technology
School of Engineering and Technology
Lakshmangarh, Rajasthan
</div>
---
<div style="page-break-after: always;"></div>
INDEX
INDEX
<table style="width:100%; border-collapse:collapse;">
  <tr>
    <th style="width:10%;">S. No.</th>
    <th style="width:65%;">Program</th>
    <th style="width:25%;">Link</th>
  </tr>
 <tr>
    <td>1</td>
    <td>Finding Execution time</td>
    <td><a href="#program-1-finding-execution-time">Program 1</a></td>
  </tr>

</table>

---
<div style="page-break-after: always;"></div>
Program 1: Finding execution time
Aim
To write a Python program to find the excution time
Program
```python
import time
start = time.time()
for i in range(1000000):
    pass
end = time.time()
print("Execution Time:", end - start, "seconds")
```
Sample Output
```text
<img width="383" height="37" alt="image" src="https://github.com/user-attachments/assets/1b1605d9-5103-4dfc-b09c-e7423fd99e60" />

```
Back to Index
---
<div style="page-break-after: always;"></div>
Program 2: Largest of Three Numbers
Aim
To write a Python program to find the largest among three numbers.
Program
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

if a >= b and a >= c:
    largest = a
elif b >= a and b >= c:
    largest = b
else:
    largest = c

print("Largest number =", largest)
```
Sample Output
```text
Enter first number: 10
Enter second number: 25
Enter third number: 15
Largest number = 25
```
Back to Index
---
<div style="page-break-after: always;"></div>
Program 3: Factorial of a Number
Aim
To write a Python program to calculate the factorial of a given number.
Program
```python
n = int(input("Enter a number: "))

fact = 1

for i in range(1, n + 1):
    fact = fact \* i

print("Factorial =", fact)
```
Sample Output
```text
Enter a number: 5
Factorial = 120
```
Back to Index
---
<div style="page-break-after: always;"></div>
Program 4: Prime Number Check
Aim
To write a Python program to check whether a given number is prime or not.
Program
```python
n = int(input("Enter a number: "))

prime = True

if n < 2:
    prime = False
else:
    for i in range(2, n):
        if n % i == 0:
            prime = False
            break

if prime:
    print(n, "is a Prime Number")
else:
    print(n, "is not a Prime Number")
```
Sample Output
```text
Enter a number: 7
7 is a Prime Number
```
Back to Index
---
<div style="page-break-after: always;"></div>
Program 5: Fibonacci Series
Aim
To write a Python program to generate the Fibonacci series.
Program
```python
n = int(input("Enter number of terms: "))

a = 0
b = 1

for i in range(n):
    print(a, end=" ")
    a, b = b, a + b
```
Sample Output
```text
Enter number of terms: 7
0 1 1 2 3 5 8
```
Back to Index
---
Example:
```python
class Student:
    def display(self):
        print("Hello")
