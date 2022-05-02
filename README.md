# -96-
d = []
for i in range(11):
    d.append([])
    for j in range(11):
        d[i].append(0)
a=[]
for i in range(10):
    a = input().split()
    for j in range(10):
        d[i+1][j+1]=int(a[j])

x,y=2,2
for _ in range(100):
    if d[x][y] == 0:  #지나간 자리를 9로 변환
        d[x][y]=9

    if d[x][y+1] == 0 :
        y+=1
    elif d[x][y+1] == 2 :
        y+=1
    elif d[x][y+1]==1:
        x+=1


    if d[x][y] == 2:
        d[x][y] = 9
        break

    if (x==9 and y==9):
        d[x][y] = 9
        break

    if (d[x+1][y]==1 and d[x][y+1]==1):
        break



for i in range(1,11):
    for j in range(1,11):
        print(d[i][j],end=' ')
    print()
