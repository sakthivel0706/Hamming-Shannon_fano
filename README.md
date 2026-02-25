# NAME : SAKTHIVEL E
# REG NO : 212224060230
# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.4,0.2,0.2,0.1,0.1} for its output. 
Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
# Tools Required:
Python IDE with Numpy and Scipy.

# Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n):
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))
    p.append(pr)
for j in range (n):
    l = float(input(f"Enter the length of the sample values {j + 1}: "))
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy
red =  round(1 - eff,3)
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
<img width="900" height="900" alt="image" src="https://github.com/user-attachments/assets/a05578a3-1f5a-47e0-9e08-aac3fb368204" />
<img width="900" height="900" alt="image" src="https://github.com/user-attachments/assets/8233b5a8-fb6c-4767-8ca3-5b0418e526ab" />
<img width="900" height="900" alt="image" src="https://github.com/user-attachments/assets/2a2c5b11-d508-44d5-bee4-06b2f484e0ce" />



# Output

<img width="478" height="290" alt="image" src="https://github.com/user-attachments/assets/ef23334c-5973-4b77-9227-562e1a1f7cdc" />

# Results:

The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
