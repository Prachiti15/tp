# tp
```
x=[]
vertices=int(input("Enter number of vertices: "))
def Hcycle(k):
  while(True):
    nextVal(k)
    if(x[k]==0):
      return
    if(k==vertices):
      print(x)
    else:
      Hcycle(k+1)

def nextVal(k):
    while(True):
      x[k]=(x[k]+1)%(vertices+1)
      if(x[k]==0):
        return
      if(G[x[k-1]][x[k]]==0):
        break
      for j in range (0,k):
        if (x[k]==x[j]):
          break
      if((k==vertices)and (G[x[k]][x[1]]==0)):
        break
      return

G = []
print("Enter the entries rowwise:")
  
# For user input
for i in range(vertices):          # A for loop for row entries
    a =[]
    for j in range(vertices):      # A for loop for column entries
         a.append(int(input()))
    G.append(a)
print("Matrix is: \n") 
# For printing the matrix
for i in range(vertices):
    for j in range(vertices):
        print(G[i][j], end = " ")
    print()
Hcycle(1)
```
