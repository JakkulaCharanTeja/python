# python
python project
names = ["charan","TEja","Ram" ]
marks=[90, 79, 75]
updates=[0, 5, 19]
n=len(marks)
def nameRank(names,marks, updates,n):
    x = [[0 for j in range(3)] for i in range (n)]
    for i in range(n):
        x[i][0] = names[i]
        x[i][1]= marks[i]+updates[i]
        x[i][2]= i+1

    highest=x[0]
    for j in range(1, n):
        if (x[j][1]>= highest[1]) :
            highest = x[j]
    print("Name:", highest[0],", Jump:",abs(highest[2]- 1),sep="")
nameRank(names,marks,updates,n)
