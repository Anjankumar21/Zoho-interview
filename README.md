1)
print("Enter size of the NxN matrix:")
n=int(input())
l=[]
c="Y"
while c=="Y":
    print("Enter the brick's position and the brick type:")
    l.append(list(map(int,input().split())))
    print("Do you want to continue(Y or N)?")
    c=input()
print("Enter ball Count")
ball=int(input())

for i in range(n):
    for j in range(n):
        checker=True
        if i==0 or j==0 or j==(n-1):
            print("W",end="")
            checker=False
        elif i==(n-1) and (j!=0 or j!=(n-1)) and j!=(n-1)//2:
            print("G", end="")
            checker=False
        elif i==(n-1) and j==(n-1)//2:
            print("o",end="")
            checker=False
        for k in l:
            if i==k[0] and j==k[1]:
                print("1",end="")
                checker=False
        if checker:
            print("", end="  ")
        else:
            print("", end=" ")
    print("")
print("Ball count is",ball)


2)
