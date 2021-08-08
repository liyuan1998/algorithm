**HJ8** **合并表记录**

## 描述

数据表记录包含表索引和数值（int范围的正整数），请对表索引相同的记录进行合并，即将相同索引的数值进行求和运算，输出按照key值升序进行输出。

### 输入描述：

先输入键值对的个数
然后输入成对的index和value值，以空格隔开

### 输出描述：

输出合并后的键值对（多行）

## 示例1

输入：

```
4
0 1
0 2
1 2
3 4
```

复制

输出：

```
0 3
1 2
3 4
```

```
n = int(input()) # 行数
l = [] # 记录输入数据表
for i in range(n):
    temp = list(map(int, input().split()))
    l.append(temp)
# print(l)
hashList = {} # store
for i in l:
    if hashList.get(i[0]) == None:
        hashList[i[0]] = i[1]
        continue
    temp = hashList[i[0]]
    tempList = []
    tempList.append(temp)
    tempList.append(i[1])
    ans = sum(tempList)
    hashList[i[0]] = ans
#print(hashList)
keyList = list(hashList.keys())
keyList.sort()
#print(keyList)
for i in keyList:
    print(i,hashList[i])
```

