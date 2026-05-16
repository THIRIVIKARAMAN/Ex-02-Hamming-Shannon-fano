# Ex: 02 - Huffman - Shannon_fano
## AIM:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average codeword length, Entropy, Variance, Redundancy, Efficiency.

## TOOLS REQUIRED:
Python IDE with Numpy and Scipy.

## PROGRAM:
~~~
import math

print("THIRIVIKARAMAN P")
print("212224060286")

L = 0
hs = 0
p = []
lk = []

n = int(input("\nEnter the number of Samples : "))

for i in range(n):
    pr = float(input(f"Enter the probability of sample values {i+1}: "))
    p.append(pr)

for j in range(n):
    l = float(input(f"Enter the length of the sample values {j+1}: "))
    lk.append(l)

for k in range(n):
    L = L + (p[k] * lk[k])

for k in range(n):
    hs = hs + (p[k] * math.log(1/p[k], 2))

eff = hs / L
red = 1 - eff

var = 0

for k in range(n):
    var = var + (p[k] * ((lk[k] - L) ** 2))

print("\nAverage Codeword Length is :", round(L, 3))
print("Entropy is :", round(hs, 3))
print("Efficiency is :", round(eff, 3))
print("Redundancy is :", round(red, 3))
print("Variance is :", round(var, 3))
~~~
## CALCULATION:
<img width="519" height="960" alt="image" src="https://github.com/user-attachments/assets/5e74c431-f813-4424-a533-8e30a2ed471b" />

## OUTPUT:
<img width="407" height="510" alt="image" src="https://github.com/user-attachments/assets/2a4dcc56-25f7-4be4-aa34-efec173f6a80" />

<img width="718" height="960" alt="image" src="https://github.com/user-attachments/assets/b606ec3d-32fd-4fd3-8b8a-f80fdbdb4be4" />



## RESULT:
The Huffman and Shannon-Fano of the given statistics {} using python are verified.
