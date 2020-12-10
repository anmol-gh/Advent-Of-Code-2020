```python
with open('aoc1.txt') as data:
        x=data.read().split('\n')
couples=[]
#Part 1

for i in range (0,len(x)):
	for j in range (i+1,len(x)):
                couples.append((int(x[i]),int(x[j])))
for i in couples:
        if sum(i)==2020:
                print('Part 1:',i[0]*i[1])
#Part 2
couples=[]
for i in range (0,len(x)):
	for j in range (i+1,len(x)):
		for k in range(j+1,len(x)):
			couples.append((int(x[i]),int(x[j]),int(x[k])))
for i in couples:
        if sum(i)==2020:
                print('Part 2:',i[0]*i[1]*i[2])
```
