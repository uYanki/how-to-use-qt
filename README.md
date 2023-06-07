[Qt 5.14](https://download.qt.io/archive/qt/5.14/) 

##### 程序导出

① 将程序编译为 release 版本

![1](.assest/1.png)

② 将编译出来 exe 复制到单独的文件夹中。

（我的在 `build-slave-Desktop_Qt_5_14_2_MinGW_32_bit-Release\release`）

此时的 exe 文件是不能运行的，会提示缺少相关的依赖文件。

③ 找到构建工具（需和 kit 对应），并通过 cd 进入到存放 exe 的文件夹中。

![2](.assest/2.png)

④ 生成依赖环境

在命令行中键入以下命令后，会出现大堆文件，：

```shell
windeployqt modbusslave.exe
```

⑤ 删除无关文件以减少文件体积（可选）

等一个一个测试，删除无关文件时不会影响程序运行的。

##### 程序打包

需安装 enigmavb

① 选择程序（exe）

② 添加文件递归（Add Folder Recursive）

③ 开启体积压缩（Compress Files）

④ 打包程序

![3](.assest/3.png)