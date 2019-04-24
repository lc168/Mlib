# Mlib
### 项目初步的设想是解决库的和头文件的，整体替换移动问题。包含一些依赖关系的处理

### 他需要回答一些关键问题
1. 编译的时候，如何找到头文件？

>>#在PATH中找到可执行文件程序的路径。
>>export PATH =$PATH:$HOME/bin (可一次指定多个搜索路径，":"用于分隔它们)
>>
>>#gcc找到头文件的路径
>>C_INCLUDE_PATH=/usr/include/libxml2:/MyLib
>>export C_INCLUDE_PATH
>>
>>#g++找到头文件的路径
>>CPLUS_INCLUDE_PATH=$CPLUS_INCLUDE_PATH:/usr/include/libxml2:/MyLib
>>export CPLUS_INCLUDE_PATH

2. 编译的时候，如何找到到库文件？

>>#找到动态链接库的路径
>>LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/MyLib 
>>export LD_LIBRARY_PATH
>>
>>#找到静态库的路径
>>LIBRARY_PATH=$LIBRARY_PATH:/MyLib
>>export LIBRARY_PATH


3. 如果编译成功，如何找到对应的库文件？
4. 如何进行版本管理？

### 解决方式:产生一个 env_bash文件来 在系统中 source
### 设置一个路径作为你的库的路径，可以进行管理和共享

>###### liucheng
>> ###### liucheng
>>```c
>>int main()
>>{
>>  printf("liucheng !\n");
>>}
>>```
