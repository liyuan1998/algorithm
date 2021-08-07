![image-20210807152301726](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210807152301726.png)

```
while True:
    try:
        n = input()
        numberHex = n.split("0x").pop()
        print(int(numberHex,16))
    except:
        break
```

python 进制转换

![image-20210807152345971](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210807152345971.png)

