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
<tr>
    <td>2</td>
    <td>Finding memory used</td>
    <td><a href="#program-2-finding-memory-used">Program 2</a></td>
  </tr>
<tr>
    <td>3</td>
    <td>Creating graph</td>
    <td><a href="#program-3-creating-graph">Program 3</a></td>
  </tr>
<tr>
    <td>4</td>
    <td>Multiple graph</td>
    <td><a href="#program-4-Multiple-graph">Program 4</a></td>
  </tr>
<tr>
    <td>5</td>
    <td>Illustrate Undirected graph</td>
    <td><a href="#program-5-Illustrate-undirected-graph">Program 5</a></td>
  </tr>
<tr>
    <td>6</td>
    <td>Illustrate directed graph</td>
    <td><a href="#program-6-Illustrate-directed-graph">Program 6</a></td>
  </tr>
<tr>
    <td>7</td>
    <td>Illustrate undirected weighted graph</td>
    <td><a href="#program-7-Illustrate-undireted-weighted-graph">Program 7</a></td>
  </tr>
<tr>
    <td>8</td>
    <td>Illustrate directed weighted graph</td>
    <td><a href="#program-8-Illustrate-directed-weighted-graph">Program 8</a></td>
  </tr>
<tr>
    <td>9</td>
    <td>Implementing BFS</td>
    <td><a href="#program-9-Implementing-BFS">Program 9</a></td>
  </tr>
  <tr>
    <td>10</td>
    <td>Implementing DFS</td>
    <td><a href="#program-10-Implementing-DFS">Program 10</a></td>
  </tr>
  <tr>
    <td>11</td>
    <td>Implementing Dijkstra fuction</td>
    <td><a href="#program-11-Implementing-Dijkstra-function">Program 11</a></td>
  </tr>
  <tr>
    <td>12</td>
    <td>Implementing Dijkstra function</td>
    <td><a href="#program-12-Implementing-Bell-Man-Ford">Program 12</a></td>
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

<img width="383" height="37" alt="image" src="https://github.com/user-attachments/assets/1b1605d9-5103-4dfc-b09c-e7423fd99e60" />


Back to Index
---
<div style="page-break-after: always;"></div>
Program 1: Finding memory used

Aim
To write a Python program to find the memory used
Program
<img width="267" height="54" alt="image" src="https://github.com/user-attachments/assets/70628998-6f14-4410-a2b9-80b27e9c2eea" />

```python
import tracemalloc

tracemalloc.start()

# Program
a = [i for i in range(100000)]

current, peak = tracemalloc.get_traced_memory()

print("Current Memory:", current, "bytes")
print("Peak Memory:", peak, "bytes")

tracemalloc.stop()
Sample Output

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
