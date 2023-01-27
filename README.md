# PL0-Compiler

## Introduction：

This program is a PL/0 language compiler written in C#. PL0 code can be compiled, P-Code generated, and run. Users can create new files to write PL0 codes, or open existing PL0 codes for editing and saving.

The UI interface is implemented using WinForm. For the error handling part, refer to Table 14.4 on page 316 of *"Compiler Principles and Compiler Program Structure"*. For the P-Code instruction set, refer to Table 15.14 on page 351. The syntax analysis part is implemented using the recursive descending subroutine method. Symbol table The management part uses a simulated stack for management.

## Error list：

            errors.Add(1, &quot;The\&quot;=\&quot;in the constant description is written as\&quot;:=\&quot;&quot;);

            errors.Add(2, &quot;The \&quot;=\&quot;in the constant description should be followed by a number&quot;);

            errors.Add(3, &quot;After the identifier in the constant declaration should be\&quot;=\&quot;&quot;);

            errors.Add(4, &quot;const, var, procedure should be followed by an identifier&quot;);

            errors.Add(5, &quot;Missing\&#39;,\&#39; or\&#39;;\&#39;&quot;);

            errors.Add(6, &quot;The symbol after the procedure description is incorrect (should be a statement start symbol, or a procedure definition symbol&quot;);

            errors.Add(7, &quot;Should be a statement start character&quot;);

            errors.Add(8, &quot;The following character in the statement part of the program body is incorrect&quot;);

            errors.Add(9, &quot;A period is missing at the end of the program\&#39;.\&#39;&quot;);

            errors.Add(10, &quot;Missing between sentences \&#39;;\&#39;&quot;);

            errors.Add(11, &quot;The identifier not specified&quot;);

            errors.Add(12, &quot;In an assignment statement, the identifier attribute on the left side of the assignment number should be a variable &quot;);

            errors.Add(13, &quot;The assignment number should be followed by the left identifier of the assignment statement\&#39;:=\&#39;&quot;);

            errors.Add(14, &quot;Call should be followed by an identifier&quot;);

            errors.Add(15, &quot;The identifier attribute after call should be a procedure &quot;);

            errors.Add(16, &quot;The conditional statements miss \&#39;then\&#39;&quot;);

            errors.Add(17, &quot;Miss\&#39;end\&#39; or\&#39;;\&#39;&quot;);

            errors.Add(18, &quot;The while-type loop statements miss\&#39;do\&#39;&quot;);

            errors.Add(19, &quot;Incorrect sign after statement&quot;);

            errors.Add(20, &quot;Should be a relational operator&quot;);

            errors.Add(21, &quot;An identifier property within an expression cannot be a procedure&quot;);

            errors.Add(22, &quot;Missing closing parenthesis in expression\&#39;)\&#39;&quot;);

            errors.Add(23, &quot;Illegal sign after factor&quot;);

            errors.Add(24, &quot;Expression cannot begin with this symbol&quot;);

            errors.Add(25, &quot;There is no until in the repeat loop statement&quot;);

            errors.Add(26, &quot;Program hierarchy exceeds limit&quot;);

            errors.Add(30, &quot;digits too long&quot;);

            errors.Add(31, &quot;number out of bounds&quot;);

            errors.Add(32, &quot;The identifier in the parentheses of the read statement is not a variable&quot;);

            errors.Add(33, &quot;Statement missing opening parenthesis\&#39;(\&#39;&quot;);

            errors.Add(34, &quot;Statement missing closing parenthesis\&#39;)\&#39;&quot;);

            errors.Add(35, &quot;The read statement lacks variables&quot;);

            errors.Add(36, &quot;Character outside program body&quot;);

## pCpde list：

 lit, lod, sto, cal, Int, jmp, jpc, opr

## How to use：

First click the file button on the menu bar and choose to open a PL/0 source code file.

![001](/image001.png)

Then click the Generate button to drop down and select compile:

![002](/image002.png)

You can see the compilation result (if there is an error, the error type and location will be prompted):

![003](/image003.png)

Then click the Generate button to drop down and select Generate, and the corresponding P-Code will be generated:

![004](/image004.png)

Finally, click the Generate button to drop down and select Run to see the results of the run:

![005](/image005.png)

## Summary：

This PL/0 compiler can be said to be the most complicated program I have completed independently since I went to college. Through writing PL/0 compiler this time, my coding ability has been greatly improved. And through hands-on practice, I have a deeper understanding of the course of compiling principles.
