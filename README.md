#启用
 1. 把下面的宏定义写入 rtconfig.h
 ```
   #define RT_USING_DFS
   #define RT_USING_MTD_NAND
   #define PKG_USING_DFS_YAFFS
```
 2. 注册 nand 驱动
 3. 调用 yaffs_start_up 注册 yaffs 驱动到'nand1'的 MTD 设备上,
    或者参照这个函数自己实现注册yaffs驱动的方法。
 4. 挂载 yaffs 文件系统
