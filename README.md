# PL0-Compiler

## Introduction：

This program is a PL/0 language compiler written in C#. PL0 code can be compiled, P-Code generated, and run. Users can create new files to write PL0 codes, or open existing PL0 codes for editing and saving.

The UI interface is implemented using WinForm. For the error handling part, refer to Table 14.4 on page 316 of *"Compiler Principles and Compiler Program Structure"*. For the P-Code instruction set, refer to Table 15.14 on page 351. The syntax analysis part is implemented using the recursive descending subroutine method. Symbol table The management part uses a simulated stack for management.

## Error list：

             errors.Add(1, "The \"=\" in the constant description is written as \":=\"");
             errors.Add(2, "The \"=\" in the constant description should be followed by a number");
             errors.Add(3, "The identifier in the constant description should be \"=\"");
             errors.Add(4, "const, var, procedure should be followed by an identifier");
             errors.Add(5, "Missing \',\' or \';\'");
             errors.Add(6, "The symbol after the process description is incorrect (should be a statement start character, or a process definer");
             errors.Add(7, "Should be a statement start character");
             errors.Add(8, "The following character of the statement part in the program body is incorrect");
             errors.Add(9, "Missing a period at the end of the program\'.\'");
             errors.Add(10, "\';\'");
             errors.Add(11, "Identifier not specified");
             errors.Add(12, "In the assignment statement, the identifier attribute on the left of the assignment number should be a variable");
             errors.Add(13, "The left identifier of the assignment statement should be followed by the assignment number \':=\'");
             errors.Add(14, "The call should be followed by an identifier");
             errors.Add(15, "Identifier property after call should be procedure");
             errors.Add(16, "Missing \'then\' in the conditional statement");
             errors.Add(17, "Missing \'end\' or \';\'");
             errors.Add(18, "\'do\' is missing in the while loop statement");
             errors.Add(19, "The symbol after the statement is incorrect");
             errors.Add(20, "Should be a relational operator");
             errors.Add(21, "Identifier attributes in expressions cannot be procedures");
             errors.Add(22, "Missing the closing parenthesis\')\'");
             errors.Add(23, "Illegal symbol after factor");
             errors.Add(24, "The beginning character of the expression cannot be this symbol");
             errors.Add(25, "There is no until in the repeat loop statement");
             errors.Add(26, "The program hierarchy exceeds the limit");
             errors.Add(30, "The number is too long");
             errors.Add(31, "Number out of bounds");
             errors.Add(32, "The identifier in the brackets of the read statement is not a variable");
             errors.Add(33, "The statement misses the left bracket\'(\'");
             errors.Add(34, "The statement misses the closing bracket\')\'");
             errors.Add(35, "The read statement lacks variables");
             errors.Add(36, "A character appears outside the program body");

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
