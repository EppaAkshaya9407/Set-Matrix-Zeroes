# Set-Matrix-Zeroes
matrix = []
r = int(input("Enter number of rows: "))
c = int(input("Enter number of columns: "))
print("Enter matrix elements:")
for i in range(r):
    row = list(map(int, input().split()))
    matrix.append(row)
rows = []
cols = []
for i in range(r):
    for j in range(c):
        if matrix[i][j] == 0:
            rows.append(i)
            cols.append(j)
for i in rows:
    for j in range(c):
        matrix[i][j] = 0
for j in cols:
    for i in range(r):
        matrix[i][j] = 0
print("Output matrix:")
for row in matrix:
    print(*row)
