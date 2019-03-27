#### 1.windows中的路径异常
```
错误信息：
"""
  File "<ipython-input-58-e0588be13bbe>", line 2
  testFile = [line.strip() for line in open("C:\Users\benqwwg\deep-learning\dataMiningTestFiles\textClassification\
  train\女性\01.txt").readlines()]                                        ^
  SyntaxError: (unicode error) 'unicodeescape' codec can't decode bytes in position 2-3: truncated \UXXXXXXXX escape
"""
原因：由于是在Windows下操作，所以路径是拷贝的，Windows下的路径分隔符默认是“\”，而“\”在python中是转义字符，且在编码是python并不会
     检验路径格式的合法性，所以在执行代码时就出错了。
解决方法：在路径字符串前面加“r”，或使用“\\”。
```
