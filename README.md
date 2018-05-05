# homework

# Exercises 4, 8,9

# Ex.9
import math
def highest_divider (n):
  a= []
  new=[]
  for i in range (2, int (math.sqrt(n))):
    if n%i== 0:
      a.append (i)
  
  
  
  for x in a:
    prime=True
    for y in range(2,x):
      if x%y ==0:
        prime=False
        
    if prime:
        new.append(x)
  return new[-1]
print(highest_divider(600851475143))
