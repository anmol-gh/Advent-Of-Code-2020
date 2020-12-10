```python
with open('input.txt') as a:
    data=a.readlines()
count=0
#Part 1
for i in data:
    min_number=i.split('-')[0]
    max_number=i.split('-')[1].split(' ')[0]
    char=i.split(' ')[1][0]
    if i.split()[-1].count(char)>=int(min_number) and i.split()[-1].count(char)<=int(max_number):
        count+=1
print('Puzzle 1:',count)
#Part 2
count=0
for i in data:
    min_number=i.split('-')[0]
    max_number=i.split('-')[1].split(' ')[0]
    password=(i.split()[-1])
    char=i.split(' ')[1][0]
    if password[int(min_number)-1]==char or password[int(max_number)-1]==char:
        if password[int(min_number)-1]==char and password[int(max_number)-1]==char:
            pass
        else:
            count+=1
print('Puzzle 2:',count)
```
