# PL0文法编译器文档

## 概述：

 本程序是使用C#编写的PL/0语言编译器。可以对PL0代码进行编译、生成P-Code、运行。用户可以新建文件编写PL0代码，或打开已有的PL0代码进行编辑并保存。

UI界面使用WinForm实现，错误处理部分参考了《编译原理及编译程序构造》第316页表14.4，P-Code指令集参考第351页表15.14，语法分析部分使用递归下降子程序法实现，符号表管理部分使用一个模拟的栈来进行管理。

## Error list：

            errors.Add(1, &quot;常数说明中的\&quot;=\&quot;写成\&quot;:=\&quot;&quot;);

            errors.Add(2, &quot;常数说明中的\&quot;=\&quot;后应是数字&quot;);

            errors.Add(3, &quot;常数说明中标识符后应是\&quot;=\&quot;&quot;);

            errors.Add(4, &quot;const, var, procedure 后应是标识符&quot;);

            errors.Add(5, &quot;漏掉了\&#39;,\&#39; 或\&#39;;\&#39;&quot;);

            errors.Add(6, &quot;过程说明后的符号不正确(应是语句开始符,或过程定义符&quot;);

            errors.Add(7, &quot;应是语句开始符&quot;);

            errors.Add(8, &quot;程序体内的语句部分的后跟符不正确&quot;);

            errors.Add(9, &quot;程序结尾丢了句号\&#39;.\&#39;&quot;);

            errors.Add(10, &quot;语句之间漏了\&#39;;\&#39;&quot;);

            errors.Add(11, &quot;标识符未说明&quot;);

            errors.Add(12, &quot;赋值语句中, 赋值号左部标识符属性应是变量&quot;);

            errors.Add(13, &quot;赋值语句左部标识符后应是赋值号\&#39;:=\&#39;&quot;);

            errors.Add(14, &quot;call 后应为标识符&quot;);

            errors.Add(15, &quot;call 后标识符属性应为过程&quot;);

            errors.Add(16, &quot;条件语句中丢了\&#39;then\&#39;&quot;);

            errors.Add(17, &quot;丢了\&#39;end\&#39; 或\&#39;;\&#39;&quot;);

            errors.Add(18, &quot;while 型循环语句中丢了\&#39;do\&#39;&quot;);

            errors.Add(19, &quot;语句后的符号不正确&quot;);

            errors.Add(20, &quot;应为关系运算符&quot;);

            errors.Add(21, &quot;表达式内标识符属性不能是过程&quot;);

            errors.Add(22, &quot;表达式中漏掉右括号\&#39;)\&#39;&quot;);

            errors.Add(23, &quot;因子后的非法符号&quot;);

            errors.Add(24, &quot;表达式的开始符不能是此符号&quot;);

            errors.Add(25, &quot;repeat 型循环语句中没有until&quot;);

            errors.Add(26, &quot;程序层次结构超过限制&quot;);

            errors.Add(30, &quot;数位太长&quot;);

            errors.Add(31, &quot;数越界&quot;);

            errors.Add(32, &quot;read语句括号中的标识符不是变量&quot;);

            errors.Add(33, &quot;语句漏掉左括号\&#39;(\&#39;&quot;);

            errors.Add(34, &quot;语句漏掉右括号\&#39;)\&#39;&quot;);

            errors.Add(35, &quot;read语句缺乏变量&quot;);

            errors.Add(36, &quot;程序体之外出现字符&quot;);

## pCpde list：

 lit, lod, sto, cal, Int, jmp, jpc, opr

## 测试流程（使用方法）：

 先点击菜单栏的文件按钮，选择打开一个PL/0源代码文件。
 
![001](https://github.com/dky815/PL0compiler/blob/master/image001.png)

然后点击生成按钮下拉选择编译：

![002](https://github.com/dky815/PL0compiler/blob/master/image002.png)

可以看到编译结果（如果有错误会提示错误类型和位置）：

![003](https://github.com/dky815/PL0compiler/blob/master/image003.png)

之后点击生成按钮下拉选择生成，就会生成相应的P-Code：

![004](https://github.com/dky815/PL0compiler/blob/master/image004.png)

最后点击生成按钮下拉选择运行可看到运行的结果：

![005](https://github.com/dky815/PL0compiler/blob/master/image005.png)

## 感想总结：

 本次PL/0编译器可以说是我上大学以来独立完成的程序中最复杂的一个，通过这次编写PL/0编译器，我的编码能力有了较大提升。并且通过动手实践，对编译原理这门课的学习也有了更深刻的理解。
