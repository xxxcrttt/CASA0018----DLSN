# 第五章. 创建应用程序
要使用模型需要将它封装在代码中，然后为代码设置必要的运行环境，提供输入并使它产生输出的行为。    
本章将创建一个嵌入式模型，建立连续循环，通过模型推断的结果打开和关闭LED。
## 5.1 详解测试 Walking Through the Tests
**测试** 是一些简短的代码片段用来演示特定的逻辑，由有效的代码组成，可以运行来证明某段代码能够实现预期的功能。  
测试能够加载模型并运行推断，来检查推断的预测值是都符合期望。它包含执行此操作所需的精确代码。
### 5.1.1 导入依赖项 Including Dependencies
```#include```是用于指定依赖项的方式，引用代码文件时定义的任何逻辑 or 变量 都可以使用。
```C++
// 训练并转换得到的正选模型，通过 xxd 转换为 C++ 代码
#include "tensorflow/lite/micro/examples/hello_world/sine_model_data.h"
// 允许解释器加载模型所需要使用的操作的类
#include "tensorflow/lite/micro/kernels/all_ops_resolver.h"
// 可以记录并输出错误以帮助调试的类
#include "tensorflow/lite/micro/micro_error_reporter.h"
// tf lite 解释器，会运行模型
#include "tensorflow/lite/micro/micro_interpreter.h"
// 用于便携测试的轻量级框架，可以帮助运行测试
#include "tensorflow/lite/micro/testing/micro_test.h"
// 定义tf lite FlatBuffer 数据结构的 schema，用于理解 .h 中的模型数据
#include "tensorflow/lite/schema/schema_generated.h"
// schema 当前版本号，根据它可以检查模型是否兼容版本的定义
#include "tensorflow/lite/version.h"
```
C++ 代码会被编写为两个文件: .cc (source file) + .h (head file)   
头文件定义允许代码连接到程序其他部分的接口，包含变量和



