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
    <td>Implementing Bell-Man-Ford</td>
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
Program 2: Finding memory used

Aim
To write a Python program to find the memory used
Program

```python

import tracemalloc

tracemalloc.start()

# Program
a = [i for i in range(100000)]

current, peak = tracemalloc.get_traced_memory()

print("Current Memory:", current, "bytes")
print("Peak Memory:", peak, "bytes")

tracemalloc.stop()
```
Sample Output
<img width="267" height="54" alt="image" src="https://github.com/user-attachments/assets/92ad0b01-ea17-4b77-8cde-e6fe5691e075" />



Back to Index
---
<div style="page-break-after: always;"></div>
Program 3: Creating graph

Aim
To write a Python program to creating graph
Program

```python
# Simple Line Graph using Text

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 30, 25]

print("Simple Line Graph")
print("X-axis:", x)
print("Y-axis:", y)
print()

for i in range(len(x)):
    print("X =", x[i], "Y =", y[i])
```

Sample Output
<img width="264" height="223" alt="WhatsApp Image 2026-10-26 at 4 36 19 PM" src="https://github.com/user-attachments/assets/41ca4739-a18c-43e6-9dbe-e0b2398b6fb0" />


Back to Index
---
<div style="page-break-after: always;"></div>
Program 4: Multiple graph

Aim
To write a Python program to Multiple graph<
Program

```python
import math

x = [1, 2, 3, 4, 5]

y1 = [math.log(i) for i in x]
y2 = [i for i in x]
y3 = [i * math.log(i) for i in x]
y4 = [i * i for i in x]

print("Line Graph Data")
print("X\tlog(x)\tx\txlog(x)\tx^2")

for i in range(len(x)):
    print(x[i], "\t", round(y1[i], 2), "\t",
          y2[i], "\t", round(y3[i], 2), "\t", y4[i])
```
Sample Output
<img width="264" height="182" alt="WhatsApp Image 2026-10-26 at 4 39 16 PM" src="https://github.com/user-attachments/assets/168eb596-26a6-4d77-919d-0e3507a07993" />

Back to Index
---
<div style="page-break-after: always;"></div>
Program 5: Illustrate Undirected graph

Aim
To write a Python program to Illustrate Undirected graph
Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")
            print()


graph = Graph()

A = graph.add_node("A")
B = graph.add_node("B")
C = graph.add_node("C")
D = graph.add_node("D")

graph.add_edge(A, B)
graph.add_edge(A, C)
graph.add_edge(B, D)
graph.add_edge(C, D)

graph.print_graph()
```
Sample Output
<img width="95" height="125" alt="WhatsApp Image 2026-10-26 at 4 41 51 PM" src="https://github.com/user-attachments/assets/d7dfc736-8f85-4211-8668-633b3591a418" />

Back to Index
---
<div style="page-break-after: always;"></div>
Program 6: Illustrate directed graph

Aim
To write a Python program to Illustrate directed graph
Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")
            print()


graph = Graph()

A = graph.add_node("A")
B = graph.add_node("B")
C = graph.add_node("C")
D = graph.add_node("D")

graph.add_edge(A, B)
graph.add_edge(A, C)
graph.add_edge(B, D)
graph.add_edge(C, D)

graph.print_graph()
```
Sample Output
<img width="93" height="112" alt="WhatsApp Image 2026-10-26 at 4 43 11 PM" src="https://github.com/user-attachments/assets/3da01c3c-3261-433e-b4f9-c7c95bfde975" />

Back to Index
---
<div style="page-break-after: always;"></div>
Program 7: Illustrate undirected weighted graph

Aim
To write a Python program to Illustrate undirected weighted graph
Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2, weight):
        node1.neighbors.append((node2, weight))
        node2.neighbors.append((node1, weight))

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor, weight in node.neighbors:
                print(f"{neighbor.data}({weight})", end=" ")
            print()


graph = Graph()

A = graph.add_node("A")
B = graph.add_node("B")
C = graph.add_node("C")
D = graph.add_node("D")

graph.add_edge(A, B, 5)
graph.add_edge(A, C, 3)
graph.add_edge(B, D, 2)
graph.add_edge(C, D, 4)

graph.print_graph()
```
Sample Output
<img width="162" height="129" alt="WhatsApp Image 2026-10-26 at 4 44 32 PM" src="https://github.com/user-attachments/assets/39bebe8f-ef96-4b65-a60a-28e9f608fea7" />

Back to Index
---
<div style="page-break-after: always;"></div>
Program 8:  Illustrate directed weighted graph

Aim
To write a Python program to  Illustrate undirected weighted graph
Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2, weight):
        node1.neighbors.append((node2, weight))

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor, weight in node.neighbors:
                print(f"{neighbor.data}({weight})", end=" ")
            print()


graph = Graph()

A = graph.add_node("A")
B = graph.add_node("B")
C = graph.add_node("C")
D = graph.add_node("D")

graph.add_edge(A, B, 5)
graph.add_edge(A, C, 3)
graph.add_edge(B, D, 2)
graph.add_edge(C, D, 4)

graph.print_graph()
```
Sample Output
<img width="141" height="109" alt="WhatsApp Image 2026-10-26 at 4 45 11 PM" src="https://github.com/user-attachments/assets/15c2c151-96f8-45eb-86a7-6f976196980d" />


Back to Index
---
<div style="page-break-after: always;"></div>
Program 9: Implementing BFS

Aim
To write a Python program to Implementing BFS
Program

```python
from collections import deque

class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []

class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    def BFS(self, start):
        visited = set()
        queue = deque([start])
        visited.add(start)

        while queue:
            node = queue.popleft()
            print(node.data, end=" ")

            for neighbor in node.neighbors:
                if neighbor not in visited:
                    visited.add(neighbor)
                    queue.append(neighbor)

# Create graph
graph = Graph()

A = graph.add_node("A")
B = graph.add_node("B")
C = graph.add_node("C")
D = graph.add_node("D")
E = graph.add_node("E")

# Add edges
graph.add_edge(A, B)
graph.add_edge(A, C)
graph.add_edge(B, D)
graph.add_edge(C, E)

# Run BFS
print("BFS Traversal:")
graph.BFS(A)
```
Sample Output
<img width="152" height="76" alt="WhatsApp Image 2026-10-26 at 4 48 22 PM" src="https://github.com/user-attachments/assets/44eaedb4-43d9-4fde-aa8f-f20151f24fd6" />

Back to Index
---
<div style="page-break-after: always;"></div>
Program 10: Implementing DFS

Aim
To write a Python program to Implementing DFS
Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    # DFS Traversal
    def DFS(self, start, visited=None):
        if visited is None:
            visited = set()

        visited.add(start)
        print(start.data, end=" ")

        for neighbor in start.neighbors:
            if neighbor not in visited:
                self.DFS(neighbor, visited)


# Create graph
graph = Graph()

A = graph.add_node("A")
B = graph.add_node("B")
C = graph.add_node("C")
D = graph.add_node("D")
E = graph.add_node("E")

# Add edges
graph.add_edge(A, B)
graph.add_edge(A, C)
graph.add_edge(B, D)
graph.add_edge(C, E)

# Run DFS
print("DFS Traversal:")
graph.DFS(A)
print()
```
Sample Output
<img width="171" height="80" alt="WhatsApp Image 2026-10-26 at 4 49 30 PM" src="https://github.com/user-attachments/assets/9c5077ec-96be-436d-a7c4-4611f2ecba38" />


Back to Index
---
<div style="page-break-after: always;"></div>
Program 11: Implementing Dijkstra fuction

Aim
To write a Python program to Implementing Dijkstra fuction
Program

```python
import heapq

class Graph:
    def __init__(self):
        self.nodes = set()
        self.neighbors = {}

    def add_node(self, node):
        self.nodes.add(node)
        self.neighbors[node] = {}
        return node

    def add_edge(self, node1, node2, weight):
        self.neighbors[node1][node2] = weight

    def dijkstra(self, source):
        distance = {node: float('inf') for node in self.nodes}
        distance[source] = 0

        priority_queue = [(0, source)]

        while priority_queue:
            current_dist, current = heapq.heappop(priority_queue)

            if current_dist > distance[current]:
                continue

            for neighbor, weight in self.neighbors[current].items():
                new_distance = current_dist + weight

                if new_distance < distance[neighbor]:
                    distance[neighbor] = new_distance
                    heapq.heappush(
                        priority_queue,
                        (new_distance, neighbor)
                    )

        return distance


# Graph Creation
g = Graph()

A = g.add_node("A")
B = g.add_node("B")
C = g.add_node("C")
D = g.add_node("D")

g.add_edge(A, B, 4)
g.add_edge(A, C, 2)
g.add_edge(C, B, 1)
g.add_edge(B, D, 3)
g.add_edge(C, D, 5)

# Call Dijkstra and Print Distances
distance = g.dijkstra(A)

print("Shortest distances from A:")
for node, dist in distance.items():
    print(node, "=", dist)
```
Sample Output
<img width="245" height="135" alt="WhatsApp Image 2026-10-26 at 4 52 42 PM" src="https://github.com/user-attachments/assets/cfe4eab3-ad25-4940-98d4-189ab40791e2" />


Back to Index
---
<div style="page-break-after: always;"></div>
Program 12: Implementing Bell-Man-Ford

Aim
To write a Python program to Implementing Bell-Man-Ford

Program

```python
class Graph:
    def __init__(self):
        self.nodes = set()
        self.edges = []

    def add_node(self, node):
        self.nodes.add(node)
        return node

    def add_edge(self, node1, node2, weight):
        self.edges.append((node1, node2, weight))

    def print_graph(self):
        print("Graph Edges:")
        for u, v, weight in self.edges:
            print(u, "->", v, "=", weight)

    def bellman_ford(self, source):
        distance = {
            node: float('inf') for node in self.nodes
        }
        distance[source] = 0

        # Relax all edges |V| - 1 times
        for _ in range(len(self.nodes) - 1):
            updated = False

            for u, v, weight in self.edges:
                if distance[u] != float('inf'):
                    new_distance = distance[u] + weight

                    if new_distance < distance[v]:
                        distance[v] = new_distance
                        updated = True

            if not updated:
                break

        # Check for a negative-weight cycle
        for u, v, weight in self.edges:
            if (distance[u] != float('inf')
                    and distance[u] + weight < distance[v]):
                print("Negative weight cycle detected!")
                return None

        return distance


# Graph Creation
g = Graph()

A = g.add_node("A")
B = g.add_node("B")
C = g.add_node("C")
D = g.add_node("D")

g.add_edge(A, B, 4)
g.add_edge(A, C, 2)
g.add_edge(B, C, -3)
g.add_edge(C, D, 5)
g.add_edge(B, D, 4)

# Print Graph
g.print_graph()

# Call Bellman-Ford and Print Distances
distance = g.bellman_ford(A)

if distance is not None:
    print("\nShortest distances from A:")
    for node, dist in distance.items():
        print(node, "=", dist)
```
Sample Output
<img width="253" height="290" alt="WhatsApp Image 2026-10-26 at 4 53 27 PM" src="https://github.com/user-attachments/assets/13d39585-1ab1-45c8-9e20-dd4c5892bcfb" />


