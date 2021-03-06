## TscanCode十月版本发布
[TscanCodeV1.10.1027.windows.exe](./release/windows/TscanCodeV1.10.1027.windows.exe)

更新列表：
1. 新增基于统计的函数返回值判空检查项；
2. 空指针、越界、未初始化误报、漏报修复；
3. 检查项优化了规则说明和Demo，规则内容一目了然；
4. UI 界面优化&bugfix；


# TscanCode
**TscanCode**是针对**C++/C#/Lua**代码的静态代码扫描解决方案，能精确发现C++空指针、Unity性能、Lua手误等问题，提高代码质量，降低代码错误修复成本。另外，TscanCode还支持C#&Lua，C++&Lua语言混合扫描，有效挖掘Unity项目跨语言交互问题。
TscanCode单机工具无需构建复杂的编译环境，一键扫描，支持用户根据不同需求自定义配置检查项，有良好的扩展性和可维护性。

TscanCode支持以下类型规则扫描：

## C++
* 空指针错误(7): 可能导致程序空指针解引用的错误
* 越界错误(7): 数组、缓冲区访问越界
* 资源泄漏错误(8): 内存或者资源（文件、管道等）泄漏错误
* 运算错误(11): sizeof, ++等运算符导致的代码错误
* 可疑错误(16): 可疑的代码错误，比如assert中进行赋值操作
* 逻辑错误(26): 不符合正常代码逻辑的代码场景
* 未初始化错误(10): 变量、结构体、指针未初始化，然后使用

## C#
* 空引用错误(6): 可能导致空对象解引用的错误场景
* 逻辑错误(22): 不符合正常代码逻辑的代码场景
* Unity特性检查(14): 针对Unity项目性能、常见错误的检查项

## Lua					 
* 未初始化(11): 检查变量初始化相关问题
* 语法错误(1): 检查语法相关问题。目前只检查括号，if-end匹配等有限的语法错误
* 跨语言交互(3): 检查Lua和C++、C#交互相关的问题
* 逻辑错误(17): 除以上三种错误以外的其他问题，如函数参数匹配，变量重名，变量类型混用等

## Docs
* [用户手册](./document/TscanCode_Manual.pdf)
* [安装系统说明](./document/TscanCode_Setup.txt)
* [现有功能&未来规划](./document/TscanCode_Plan.txt)
* [已知故障](./document/TscanCode_Bug.txt)

## FAQ
[TscanCode常见问题](https://github.com/Tencent/TscanCode/wiki/TscanCode常见问题)

