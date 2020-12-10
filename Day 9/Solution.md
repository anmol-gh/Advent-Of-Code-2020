```python
def day9p1(file_name,step):
    from itertools import combinations
    with open(file_name)as f:
        number_lst,i,count=f.read().split('\n'),0,0
    while True:
        for k in list(combinations(number_lst[i:step+i],2)):
            if int(number_lst[i+step])==(int(k[0])+int(k[-1])):
                i+=1
                count=0
                break
            else:
                count+=1
                if count==300:
                    return 'First Part: '+number_lst[i+step]
print(day9p1('input.txt',25))
def day9p2(file_name):
    index,count,sums=0,0,[]
    number_lst=open(file_name).read().split('\n')
    while True:
        variable=0
        for i in range(0,1000):
            count+=int(number_lst[index+variable])
            sums.append(int(number_lst[index+variable]))
            variable+=1
            if count>400480901:
                index+=1
                sums,count,variable=[],0,0
            elif count==400480901:
                return 'Second Part: '+str(min(sums)+max(sums))
print(day9p2('input.txt'))
```
