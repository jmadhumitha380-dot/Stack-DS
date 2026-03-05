# Stack-DS
Practice program
q = int(input())

s = ""
history = []

for _ in range(q):
    query = input().split()

    if query[0] == '1':        # append
        history.append(s)
        s += query[1]

    elif query[0] == '2':      # delete
        history.append(s)
        k = int(query[1])
        s = s[:-k]

    elif query[0] == '3':      # print
        k = int(query[1])
        print(s[k-1])

    elif query[0] == '4':      # undo
      s = history.pop()
sample iinput
8
1 abc
3 3
2 3
1 xy
3 2
4
4
3 1
sample Output:
c
y
a
