# Mlib
### 项目初步的设想是解决库的和头文件的，整体替换移动问题。包含一些依赖关系的处理

### 他需要回答一些关键问题
1. 编译的时候，如何找到头文件？
2. 编译的时候，如何找到到库文件？
3. 如果编译成功，如何找到对应的库文件？
4. 如何进行版本管理？

### 解决方式:产生一个 env_bash文件来 在系统中 source
### 设置一个路径作为你的库的路径，可以进行管理和共享
