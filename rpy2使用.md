### 安装
`
conda create -n py37 python=3.7  
`

`
pip install rpy2
`

### 设置环境变量
windows参考https://blog.csdn.net/qq_31342997/article/details/89428158  
Linux参考https://www.cnblogs.com/cloudtj/articles/6372197.html

例如环境变量需要设置成以下形式：
![image](https://user-images.githubusercontent.com/46037197/164277306-f22f48c4-4df0-4d4d-bf78-6f076a577089.png)

可以在终端运行以下命令查看环境是否配置好 

`
python -m rpy2.situation
`

如果有下图情况，说明配置好了，其中rpy2正确找到R
![image](https://user-images.githubusercontent.com/46037197/164277801-c91321ce-a205-4711-b1c1-e9627022f2aa.png)

