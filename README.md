## ExpNo 4 : Implement A* search algorithm for a Graph
#### Name: Saravanan N
#### Register Number/Staff Id: TSML006

## Name: Selvakumar A
## Register Number: 212222110042

## Aim:

To ImplementA * Search algorithm for a Graph using Python 3.
## Algorithm:

``````
## Algorithm:
```
// A* Search Algorithm
1.  Initialize the open list
2.  Initialize the closed list
    put the starting node on the open 
    list (you can leave its f at zero)
3.  while the open list is not empty
    a) find the node with the least f on 
       the open list, call it "q"
    b) pop q off the open list
  
    c) generate q's 8 successors and set their 
       parents to q
   
    d) for each successor
        i) if successor is the goal, stop search
        
        ii) else, compute both g and h for successor
          successor.g = q.g + distance between 
                              successor and q
@@ -32,26 +30,20 @@ To ImplementA * Search algorithm for a Graph using Python 3.
          ways, we will discuss three heuristics- 
          Manhattan, Diagonal and Euclidean 
          Heuristics)
          
          successor.f = successor.g + successor.h
        iii) if a node with the same position as 
            successor is in the OPEN list which has a 
           lower f than successor, skip this successor
        iV) if a node with the same position as 
            successor  is in the CLOSED list which has
            a lower f than successor, skip this successor
            otherwise, add  the node to the open list
     end (for loop)
  
    e) push q on the closed list
    end (while loop)
```

``````


## Program:
## PROGRAM:
```
from collections import defaultdict
H_dist ={}
@@ -62,7 +54,8 @@ def aStarAlgo(start_node, stop_node):
    parents = {}         # parents contains an adjacency map of all nodes
    #distance of starting node from itself is zero
    g[start_node] = 0
```
```
#start_node is root node i.e it has no parent nodes
#so start_node is set to its own parent node
@@ -98,6 +91,7 @@ while len(open_set) > 0:
    if n == None:
        print('Path does not exist!')
        return None
        
# if the current node is the stop_node
# then we begin reconstructin the path from it to the start_node
@@ -116,7 +110,8 @@ while len(open_set) > 0:
    closed_set.add(n)
print('Path does not exist!')
return None
```
```
#define fuction to return neighbor and its distance
@@ -156,69 +151,67 @@ Graph_nodes=graph
print(graph)
aStarAlgo('S', 'G')
```
##  Sample Graph I


![image](https://github.com/natsaravanan/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/87870499/b1377c3f-011a-4c0f-a843-516842ae056a)


## Sample Input

10 14 <br>
A B 6 <br>
A F 3 <br>
B D 2 <br>
B C 3 <br>
C D 1 <br>
C E 5 <br>
D E 8 <br>
E I 5 <br>
E J 5 <br>
F G 1 <br>
G I 3 <br>
I J 3 <br>
F H 7 <br>
I H 2 <br>
A 10 <br>
B 8 <br>
C 5 <br>
D 7 <br>
E 3 <br>
F 6 <br>
G 5 <br>
H 3 <br>
I 1 <br>
J 0 <br>
<hr>
<h2>Sample Output</h2>
<hr>
## Sample Graph I:

![image](https://github.com/22008686/19AI405ExpNo4/assets/118916413/25326942-3034-4607-8da1-eb110ae5752a)

## Sample Input:

10 14
A B 6
A F 3
B D 2
B C 3
C D 1
C E 5
D E 8
E I 5
E J 5
F G 1
G I 3
I J 3
F H 7
I H 2
A 10
B 8
C 5
D 7
E 3
F 6
G 5
H 3
I 1
J 0

## Sample Output:

Path found: ['A', 'F', 'G', 'I', 'J']

## Sample Graph II:

![image](https://github.com/22008686/19AI405ExpNo4/assets/118916413/f4e348fe-235e-4b57-8d62-024f97003ba6)

## Sample Input:

6 6
A B 2
B C 1
A E 3
B G 9
E D 6
D G 1
A 11
B 6
C 99
E 7
D 1
G 0

## Sample Output:

<hr>
<h2>Sample Graph II</h2>
<hr>

![image](https://github.com/natsaravanan/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/87870499/acbb09cb-ed39-48e5-a59b-2f8d61b978a3)


<hr>
<h2>Sample Input</h2>
<hr>
6 6 <br>
A B 2 <br>
B C 1 <br>
A E 3 <br>
B G 9 <br>
E D 6 <br>
D G 1 <br>
A 11 <br>
B 6 <br>
C 99 <br>
E 7 <br>
D 1 <br>
G 0 <br>
<hr>
<h2>Sample Output</h2>
<hr>
Path found: ['A', 'E', 'D', 'G']

## RESULT:

Implementing A * Search algorithm for a Graph using Python 3. is executed successfully.
