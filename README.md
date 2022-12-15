# domain-specific-language-in-go

### 内部数据结构

##### Symbol

一张表,记录脚本中出现的所有非字面值,map记录一个symbol是变量名,块名,关键字还是函数名.

##### Variables

map变量名到变量值.

##### Blocks

map变量名到block对象.



- 关键字

var
switch, default 在parse阶段就被分解为一条条match语句存储到Block中的statements

- var

用map记录各个变量的值,使用自定的Variable类型,其中指明了变量的类型和值,值总是用string存储,在解析时翻译为对应的类型.

- begin

- 函数
函数的功能有很多,包括在块之间跳转(goto函数)以及修改变量的值

- switch



ref:

[Build your own DSL with Go & HCL](https://blog.devgenius.io/build-your-own-dsl-with-go-hcl-602c92ce24c0)

[Abusing Go Syntax to Create a Domain-Specific Language](https://blog.gopheracademy.com/advent-2016/go-syntax-for-dsls/)















大作业
- 代码审查、功能验证、技术提问、文档检查
- 占成绩70%

程序题目：一种领域特定脚本语言的解释器的设计与实现

描述：领域特定语言（DomainSpecificLanguage，DSL）可以提供一种相对简单的文法，用于特定领域的业务流程定制。本作业要求**定义一个领域特定脚本语言**，这个语言能够描述在线客服机器人（机器人客服是目前提升客服效率的重要技术，在银行、通信和商务等领域的复杂信息系统中有广泛的应用）的自动应答逻辑，并**设计实现一个解释器解释执行这个脚本**，可以根据用户的不同输入，根据脚本的逻辑设计给出相应的应答。

基本要求：
- 脚本语言的语法可以自由定义，只要语义上满足描述客服机器人自动应答逻辑的要求。
- 程序输入输出形式不限，可以简化为纯命令行界面。
- 应该给出几种不同的脚本范例，对不同脚本范例解释器执行之后会有不同的行为表现。



风格：满分15分，其中代码注释6分，命名6分，其它3分。
设计和实现：满分30分，其中**数据结构7分，模块划分7分，功能8分，文档8分。**
接口：满分15分，其中程序间接口8分，人机接口7分。
测试：满分30分，测试桩15分，自动测试脚本15分
记法：满分10分，文档中对此脚本语言的语法的准确描述。
