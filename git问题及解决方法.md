#git使用时出现的问题和解决方法
## 1 .gitignore无法过滤一些文件
原因：在git库中已经存在该文件，已经进行过add操作
方法：执行
``` 
find . -iname "file_or_directory_name" -type d -exec git rm -rf --cached  {} \;
```

