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


# ex.8
def longestSubSequence(str1,str2):
  biggest_size = 0
  str = ""
  size = 0
  for i in range(len(str1)):
    start = i
    for j in range(len(str2)):
      if(str1[i] == str2[j]):
        i=i+1
        size = size + 1
      else:
        if(size > biggest_size):
          biggest_size = size
          str = str1[start-1:start+size]
        size = 0
      print(str)
  
  
  
def main():
  longestSubSequence("fddog","dddddog")
  
main()

# Ex.4

translation=input("Type a text to be translated to Pig Latin: ")
def pig_Latin(l):
    a = l.lower()
    b = l.split()
    d = ""
    for n in b:
        first = n[0]
        word = n[1:]
        new_word=word+first+"ay "
        d=d+new_word
    return d


print(pig_Latin(translation))
