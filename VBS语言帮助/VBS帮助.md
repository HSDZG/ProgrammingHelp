# VBS帮助文档
[toc]

## 概述
[开头](#vbs帮助文档)
VBS（Visual Basic Scripting）是一种基于微软的Visual Basic语言的脚本语言。它是一种解释性语言，旨在使用脚本来自动化任务和处理Windows环境中的各种操作。

以下是关于VBS的一些概述信息：

1. 语法和特性：VBS的语法与Visual Basic类似，但与Visual Basic有一些差异。它是一种弱类型语言，支持自动变量声明。VBS支持面向对象编程（OOP），包括类、对象和方法。它还支持控制流语句（如条件判断和循环）以及常见的操作符（如算术和逻辑操作符）。

2. 执行环境：VBS主要是为Windows操作系统环境开发的，可以在Microsoft Windows操作系统中的各种应用程序（如Windows脚本宿主、Internet Explorer、Office应用等）中执行。

3. 用途和功能：VBS常用于自动化任务和系统管理。它可以用于编写登录脚本、任务计划、自动化测试、文件处理、注册表操作以及与COM（Component Object Model）组件的交互等。VBS还可以通过Windows脚本宿主（wscript.exe和cscript.exe）执行，并与操作系统和应用程序进行交互。

4. 学习和资源：VBS有很多教程、文档和在线资源可用于学习和参考。微软官方提供了详细的VBS文档，包括语法参考和示例。此外，还有许多第三方网站、书籍和论坛提供VBS的学习资源和实用技巧。

需要注意的是，尽管VBS在一些场景中仍然有用，但它的使用已经逐渐被其他编程语言和技术所替代，特别是PowerShell和Python等更强大和灵活的脚本语言。因此，在考虑使用VBS之前，建议评估其他可用的工具和语言，以选择最适合你的任务和目标的解决方案。

## 开发环境
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）开发中，你可以使用各种编辑器和集成开发环境（IDE）来编写和运行VBS脚本。以下是几种常见的VBS开发环境：

1. Windows记事本（Notepad）：Windows操作系统自带的记事本编辑器可以用于编写VBS脚本。你可以使用它打开空白文本文件，并将VBS代码粘贴到其中。然后，将文件保存为.vbs扩展名，例如"script.vbs"。在Windows中双击该脚本文件将会执行它。

2. Visual Studio Code：Visual Studio Code是一个轻量级的代码编辑器，可以通过安装扩展来支持VBS开发。你可以安装"Visual Basic"扩展来提供VBS语法高亮显示、代码补全和其他有用的功能。

3. Notepad++：Notepad++是一个功能强大的文本编辑器，支持多种编程语言，包括VBS。它提供了语法高亮显示、自动完成、缩进和多文件编辑等功能，可提升VBS开发的效率。

4. Visual Studio：如果你想使用更强大的开发环境，可以考虑使用Visual Studio。尽管Visual Studio主要面向开发Windows应用程序，但它也提供了对VBS脚本的支持。你可以创建一个"Windows脚本"项目，然后在其中编写和调试VBS代码。

无论你选择哪种开发环境，编写好的VBS脚本可以通过双击脚本文件或使用Windows脚本宿主（wscript.exe或cscript.exe）来运行。Windows脚本宿主是Windows操作系统的一部分，用于解析和执行VBS脚本。

## 基本语法
[开头](#vbs帮助文档)
在VBS中，每条语句的结尾通常不需要使用分号（`;`），因为VBS不强制要求在每条语句的结尾使用分号作为结束符号。在VBS中，语句可以通过换行符或关键字作为分隔符来进行区分。

例如，下面是一些常见的VBS语句示例，它们没有在末尾使用分号：

```vbscript
variable = 10
If condition Then
    MsgBox "Condition is true"
End If
For i = 1 To 5
    MsgBox i
Next
```

尽管如此，在某些情况下，您可以选择在语句的末尾使用分号。使用分号是可选的，并且可以用于在同一行上编写多个语句。这在一些编码规范或个人偏好中可能会有所要求。

```vbscript
variable = 10; MsgBox "Value: " & variable
```

请注意，在使用分号时要小心避免过度使用，以保持代码的可读性和清晰性。

总而言之，虽然VBS中的分号是可选的，但通常情况下，不需要在每条语句的结尾使用分号。

## 注释
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，注释是用来解释和说明代码的文本，不会被执行或编译。在VBS中，有两种常见的注释方式：

1. 单行注释：在单独一行上添加注释内容，以 `'` 符号开头。VBS会忽略 `'` 符号后面的内容。

   示例：
   ```vbscript
   ' 这是一条单行注释
   variable = 10 ' 这是对变量赋值的注释
   ```
  
2. 多行注释：多行注释可以用于一段连续的注释内容，使用 `Rem` 关键字作为开始，使用 `End Rem` 关键字作为结束。`Rem` 和 `End Rem` 必须单独占据一行。

   示例：
   ```vbscript
   Rem 这是一段多行注释
   可以包含多行内容
   End Rem
   ```

注释对于向其他开发者或自己解释代码的目的非常有用。您可以使用注释来记录代码功能、变量用途、算法解释等。

虽然注释不会被VBS执行，但在阅读代码和维护代码时，注释对于理解代码的逻辑和意图非常重要。良好的注释能够提高代码的可读性和可维护性。

## 标识符
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，标识符用于给变量、函数、过程等命名。标识符是用来识别和引用代码中的不同元素的名称。VBS中的标识符需要遵循以下规则：

1. 标识符可以包含字母、数字和下划线（_）字符。
2. 标识符必须以字母或下划线（_）字符开头，不能以数字开头。
3. 标识符不区分大小写，但通常使用驼峰命名法。
4. 标识符不能是VBS的保留字或关键字。

以下是一些有效的VBS标识符示例：

```vbscript
myVariable
MyFunction
_count
first_name
TotalAmount
```

请注意，标识符的选择对于代码的可读性和理解性非常重要。使用具有描述性的标识符名称可以使代码更易读，同时也能更好地传达变量、函数或过程的用途和功能。

此外，遵循一致的命名规范和约定对于团队合作和代码维护也很重要，可以提高代码的可读性和可维护性。

## 关键字
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，关键字是预定义的特殊单词，具有固定的含义和功能。这些关键字在VBS中具有特殊的语法和上下文使用。

下面是一些常见的VBS关键字示例：

1. `Dim`：用于声明变量。
2. `If`、`Then`、`Else`、`ElseIf`、`End If`：用于条件语句，用于根据特定条件执行不同的操作。
3. `For`、`Next`：用于循环语句，用于重复执行一段代码块一定次数。
4. `Do`、`While`、`Loop`：用于循环语句，用于根据特定条件重复执行一段代码块。
5. `Sub`、`End Sub`：用于定义和结束过程。
6. `Function`、`End Function`：用于定义和结束函数。
7. `Call`：用于调用过程或函数。
8. `Exit`：用于退出循环或过程。
9. `True`、`False`：布尔值。
10. `And`、`Or`、`Not`：用于逻辑运算。
11. `ByVal`、`ByRef`：用于指定参数的传递方式。
12. `Exit Do`、`Exit For`、`Exit Function`、`Exit Sub`：用于提前结束循环、函数或过程。

以上只是一些常见的VBS关键字示例，VBS中还有其他关键字，用于执行特定的操作和控制流程。

请注意，在编写VBS代码时，关键字是保留的，不能用作标识符（变量名、函数名等）。

## 基本输入输出
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，有几种基本的输入输出方式可以与用户交互和显示结果。以下是一些常见的VBS输入输出方法：

1. `MsgBox`：用于显示消息框来输出信息或显示警告、错误等。它可以显示文本和按钮，用户可以点击按钮进行交互。

   示例：
   ```vbscript
   MsgBox "Hello, World!" ' 显示消息框输出文本
   ```

2. `InputBox`：用于弹出输入框，用户可以在输入框中输入内容，然后脚本可以读取用户输入的信息。

   示例：
   ```vbscript
   userInput = InputBox("请输入您的姓名：") ' 弹出输入框并获取用户输入
   MsgBox "您输入的姓名是：" & userInput ' 显示用户输入的姓名
   ```

3. `WScript.StdIn`：用于从命令行或控制台接收用户输入的数据。

   示例：
   ```vbscript
   Set objStdIn = WScript.StdIn ' 创建 WScript 对象来接收输入
   userInput = objStdIn.ReadLine() ' 从命令行读取用户输入的行
   WScript.Echo "您输入的内容是：" & userInput ' 显示用户输入的内容
   ```

4. `WScript.Echo`：用于向控制台输出文本或变量的值。

   示例：
   ```vbscript
   variable = "Hello, World!"
   WScript.Echo variable ' 输出变量的值到控制台
   ```

这些是VBS中一些基本的输入输出方法。您可以根据需要选择适合您的具体应用场景的方法。

### MsgBox
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，`MsgBox`函数用于显示一个消息框，将信息呈现给用户并等待用户的响应。`MsgBox`函数的语法如下：

```vbscript
MsgBox(prompt[, buttons] [, title] [, helpfile, context])
```

参数说明：
- `prompt`：必需，要显示的消息字符串。
- `buttons`：可选，指定消息框中显示的按钮组合。
- `title`：可选，指定消息框的标题。
- `helpfile`：可选，指定帮助文件的路径。
- `context`：可选，指定帮助文件中的上下文号码。

`MsgBox`函数会返回用户的响应结果。常见的按钮组合包括：
- `vbOKOnly`：显示一个确定按钮。
- `vbOKCancel`：显示确定和取消按钮。
- `vbAbortRetryIgnore`：显示中止、重试和忽略按钮。
- `vbYesNoCancel`：显示是、否和取消按钮。
- `vbYesNo`：显示是和否按钮。
- `vbRetryCancel`：显示重试和取消按钮。

以下是一个示例：

```vbscript
result = MsgBox("Hello, World!", vbOKCancel, "提示")
If result = vbOK Then
    MsgBox "用户点击了确定按钮！"
ElseIf result = vbCancel Then
    MsgBox "用户点击了取消按钮！"
End If
```

在上面的示例中，显示了一个消息框，其中包含"Hello, World!"的消息，并显示确定和取消按钮。根据用户的响应，显示不同的消息框。


### InputBox
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，`InputBox`函数用于显示一个输入框，允许用户输入文本数据，并返回用户输入的值。`InputBox`函数的语法如下：

```vbscript
InputBox(prompt[, title] [, default] [, xpos] [, ypos] [, helpfile, context])
```

参数说明：
- `prompt`：必需，要显示的提示消息字符串。
- `title`：可选，指定输入框的标题。
- `default`：可选，指定输入框中的默认值。
- `xpos`：可选，指定输入框的水平位置。
- `ypos`：可选，指定输入框的垂直位置。
- `helpfile`：可选，指定帮助文件的路径。
- `context`：可选，指定帮助文件中的上下文号码。

`InputBox`函数会弹出一个对话框，用户可以在输入框中输入文本，并返回用户输入的值。

以下是一个示例：

```vbscript
name = InputBox("请输入您的姓名：", "输入框示例", "John Doe")
MsgBox "您输入的姓名是：" & name
```

在上面的示例中，会弹出一个输入框提示用户输入姓名。输入框的标题为"输入框示例"，默认值为"John Doe"。输入的姓名将存储在变量`name`中，然后通过`MsgBox`函数显示出来。

当用户点击确认按钮时，`InputBox`函数会返回用户输入的值。如果用户点击取消按钮，函数将返回空字符串。

## 文件输入输出
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，您可以使用文件输入和输出来读取和写入文件中的数据。以下是VBS中一些常用的文件输入输出方法：

1. 文件输入（读取文件）：
   ```vbscript
   ' 打开文件
   Set objFSO = CreateObject("Scripting.FileSystemObject")
   Set objFile = objFSO.OpenTextFile("C:\path\to\file.txt", 1)

   ' 逐行读取文件内容
   Do Until objFile.AtEndOfStream
       strLine = objFile.ReadLine()
       ' 处理文件内容
       ' ...
   Loop

   ' 关闭文件
   objFile.Close
   ```

2. 文件输出（写入文件）：
   ```vbscript
   ' 创建文件
   Set objFSO = CreateObject("Scripting.FileSystemObject")
   Set objFile = objFSO.CreateTextFile("C:\path\to\file.txt", True)

   ' 写入内容到文件
   objFile.WriteLine "Hello, World!"
   objFile.Write "Number: "
   objFile.Write 123

   ' 关闭文件
   objFile.Close
   ```

在上述示例中，首先创建了 `FileSystemObject` 对象，用于处理文件操作。然后使用 `OpenTextFile` 方法打开文件以便读取内容，或使用 `CreateTextFile` 方法创建文件以便写入内容。

对于文件输入，可以使用 `ReadLine` 方法逐行读取文件内容，直到到达文件末尾 (`AtEndOfStream`)。您可以在循环中处理每一行的内容。

对于文件输出，可以使用 `WriteLine` 或 `Write` 方法写入内容到文件中。`WriteLine` 方法用于写入一个完整的行，而 `Write` 方法用于连续写入内容。

最后，别忘记使用 `Close` 方法关闭文件，释放资源。

请注意，对于文件操作，确保拥有适当的权限来读取或写入文件，并确保指定了正确的文件路径。

## 数据类型
### 基本数据类型
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，有几种基本的数据类型用于存储不同类型的数据。以下是VBS中常见的基本数据类型：

1. 整数类型（Integer）：用于存储整数值。
   ```vbscript
   Dim num As Integer
   num = 10
   ```

2. 长整数类型（Long）：用于存储较大范围的整数值。
   ```vbscript
   Dim largeNum As Long
   largeNum = 1234567890
   ```

3. 单精度浮点数类型（Single）：用于存储小数值，具有较低的精度。
   ```vbscript
   Dim floatValue As Single
   floatValue = 3.14
   ```

4. 双精度浮点数类型（Double）：用于存储小数值，具有较高的精度。
   ```vbscript
   Dim doubleValue As Double
   doubleValue = 3.14159
   ```

5. 字符串类型（String）：用于存储文本数据。
   ```vbscript
   Dim name As String
   name = "John Doe"
   ```

6. 布尔类型（Boolean）：用于存储逻辑值，只能为 True 或 False。
   ```vbscript
   Dim isTrue As Boolean
   isTrue = True
   ```

7. 日期类型（Date）：用于存储日期和时间值。
   ```vbscript
   Dim currentDate As Date
   currentDate = Now()
   ```

8. 对象类型（Object）：用于存储引用其他对象的值。
   ```vbscript
   Dim obj As Object
   Set obj = CreateObject("Scripting.FileSystemObject")
   ```

这些是VBS中的一些基本数据类型。VBS是一种弱类型语言，变量的类型可以根据赋给它们的值自动确定。因此，不需要明确声明变量的数据类型。例如，`Dim num` 将会创建一个变量 `num` 而不指定其数据类型，它会根据所赋的值自动确定。

### 变量
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，变量是用于存储和操作数据的容器。在使用变量之前，需要先声明变量并指定其名称和数据类型（可选）。以下是一些关于VBS变量的常见用法和规则：

1. 变量的声明：
   ```vbscript
   Dim variableName
   Dim variableName As DataType
   ```

   使用 `Dim` 关键字声明变量。变量名称可以使用字母、数字和下划线，并且不能以数字开头。例如：`Dim num, name, age As Integer`。

2. 变量的赋值：
   ```vbscript
   variableName = value
   ```

   使用 `=` 运算符将值赋给变量。例如：`num = 10`。

3. 变量的使用：
   ```vbscript
   result = num1 + num2
   MsgBox "The result is: " & result
   ```

   可以使用变量进行各种计算和操作。变量可以参与数学运算、连接字符串、调用函数等。

4. 变量的数据类型：
   VBS是一种弱类型语言，变量的数据类型可以根据所赋的值自动确定。例如，`Dim num` 将会创建一个变量 `num` 而不指定其数据类型，它会根据所赋的值自动确定。

   可以显式指定变量的数据类型，如：
   ```vbscript
   Dim age As Integer
   Dim name As String
   ```

   在VBS中常见的数据类型有整数类型（Integer）、长整数类型（Long）、单精度浮点数类型（Single）、双精度浮点数类型（Double）、字符串类型（String）、布尔类型（Boolean）、日期类型（Date）等。

5. 变量的作用域：
   在VBS中，可以在局部作用域（过程或函数内部）或全局作用域（模块级别）中声明变量。例如，在子过程或函数内部声明的变量只在该过程或函数内部可见。

   具体的作用域规则可以根据变量的声明位置和具体情况而定。

6. 变量命名规则：
   - 变量名只能包含字母、数字和下划线。
   - 变量名不能以数字开头。
   - 变量名区分大小写。
   - 变量名应具有描述性，以便在代码中易于理解和识别。
   - 避免使用与VBS关键字相同的名称作为变量名。

请注意，VBS是一种动态的脚本语言，变量的类型可以根据赋给它们的值自动确定。因此，不需要在声明变量时显式指定其数据类型，除非需要特定的类型。

### 常量
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，常量是指在程序中固定不变的值。使用常量可以让代码更易读、易于理解，并且便于日后维护。以下是一些常见的VBS常量：

1. 数字常量：
   - `True`：表示逻辑真值。
   - `False`：表示逻辑假值。
   - `Empty`：表示一个未初始化或未赋值的变量。
   - `Null`：表示一个空值或未知值。
   - `Pi`：表示圆周率的近似值（3.14159）。

2. 字符串常量：
   - `vbCr`：表示回车（Carriage Return）字符。
   - `vbLf`：表示换行（Line Feed）字符。
   - `vbCrLf`：表示回车和换行组合。
   - `vbTab`：表示水平制表符（Tab）字符。

3. 键盘常量：
   - `vbKeyBack`：表示退格键。
   - `vbKeyReturn`：表示回车键。

4. 对话框常量：
   - `vbOKOnly`：只显示 OK 按钮。
   - `vbOKCancel`：显示 OK 和 Cancel 按钮。
   - `vbYesNo`：显示 Yes 和 No 按钮。

这些常量提供了对常见值的简单标识，以便在代码中使用。常量的值在程序运行时是不可修改的。您可以直接使用这些常量，例如：

```vbscript
MsgBox "Hello", vbOKOnly
```

上述示例中，使用 `vbOKOnly` 常量指定了一个只有 OK 按钮的对话框。

除了内置的常量外，您也可以自定义常量，通过使用 `Const` 关键字声明一个常量，并为其指定一个值。例如：

```vbscript
Const MAX_VALUE = 100
```

上述示例中，定义了一个名为 `MAX_VALUE` 的常量，并将其值设置为 100。在接下来的代码中，可以使用 `MAX_VALUE` 来引用该常量。

请注意，根据编程的上下文，还可以使用其他常量，或使用运算符和表达式生成常量值。

### 转义字符 
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，转义字符用于表示特殊字符和控制字符。它们使用反斜杠（\）作为前缀，后跟一个或多个字符。以下是VBS中常用的转义字符：

1. `\"`：表示双引号（"）字符。
   ```vbscript
   Dim message
   message = "He said, \""Hello\"" to me."
   ```

2. `\'`：表示单引号（'）字符。
   ```vbscript
   Dim text
   text = 'It\'s a beautiful day.'
   ```

3. `\\`：表示反斜杠（\）字符。
   ```vbscript
   Dim path
   path = "C:\\Program Files\\"
   ```

4. `\n`：表示换行（新行）字符。
   ```vbscript
   Dim lines
   lines = "Line 1" & vbCrLf & "Line 2"
   MsgBox lines
   ```

5. `\t`：表示水平制表符（Tab）字符。
   ```vbscript
   Dim tabs
   tabs = "Col1" & vbTab & "Col2" & vbTab & "Col3"
   MsgBox tabs
   ```

6. `\r`：表示回车（Carriage Return）字符。

这些转义字符允许您在字符串中插入特殊字符，包括引号以及控制字符，如换行符和制表符。通过使用转义字符，您可以在字符串中包含具有特殊含义的字符，而不会产生语法错误。

请注意，VBS对转义字符的支持可能有所差异。在一些特定的环境或应用程序中，可能需要使用不同的转义字符语法或特殊的字符串处理方法。

### 复合类型
#### 数组
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，数组是一种用于存储和管理多个相关值的数据结构。数组在声明时需要指定数组的大小，并可以通过索引访问和修改数组中的元素。以下是在VBS中使用数组的基本操作方法：

1. 声明数组：
   ```vbscript
   Dim arr(5)      ' 声明一个包含6个元素的一维数组
   Dim matrix(3,3) ' 声明一个4x4的二维数组
   ```

   在声明数组时，需要指定数组的大小，可以是一个或多个维度。数组的索引从 0 开始，因此上述示例中的一维数组 `arr` 的索引范围是 0 到 5，二维数组 `matrix` 的索引范围是 0 到 3。

2. 赋值和访问数组元素：
   ```vbscript
   arr(0) = 10             ' 给数组元素赋值
   value = arr(0)          ' 访问数组元素的值
   ```

   数组的元素可以通过索引访问和赋值。上述示例中，将数组 `arr` 的第一个元素赋值为 10，并使用 `arr(0)` 访问该元素。

3. 获取数组大小：
   ```vbscript
   size = UBound(arr) + 1  ' 获取数组的大小
   ```

   使用 `UBound` 函数可以获取数组的最大索引值。对于一维数组，可以通过将 `UBound` 函数的返回值加 1 获取数组的大小。

4. 遍历数组：
   ```vbscript
   For i = 0 To UBound(arr)
       ' 访问数组元素 arr(i)
       ' ...
   Next
   ```

   可以使用循环语句（如 `For` 循环）遍历数组中的所有元素。通过循环遍历每个索引值，您可以访问数组中的每个元素。

数组的大小在声明时确定，一旦声明后，大小通常是固定的。如果需要动态调整数组的大小，可以使用 `ReDim` 语句重新调整数组的大小。

VBS还支持多维数组，您可以使用逗号分隔的索引来访问（如 `arr(0, 0)`）。多维数组在处理矩阵、表格等数据时非常有用。

#### 多维数组
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，多维数组可以存储和处理具有多个维度的数据，比如矩阵、表格等。在VBS中，使用逗号分隔的索引来访问和操作多维数组的元素。以下是在VBS中使用多维数组的示例：

1. 声明多维数组：
   ```vbscript
   Dim matrix(3, 3)     ' 声明一个4x4的二维数组
   Dim cube(2, 2, 2)    ' 声明一个3x3x3的三维数组
   ```

   在声明多维数组时，需要指定每个维度的大小。以上示例中的二维数组 `matrix` 的索引范围是 0 到 3，三维数组 `cube` 的索引范围是 0 到 2。

2. 赋值和访问多维数组的元素：
   ```vbscript
   matrix(0, 0) = 10             ' 给数组元素赋值
   value = matrix(0, 0)          ' 访问数组元素的值
   ```

   多维数组的元素可以使用逗号分隔的索引访问和赋值。上述示例中，将二维数组 `matrix` 的第一个元素赋值为 10，并使用 `matrix(0, 0)` 访问该元素。

3. 遍历多维数组：
   ```vbscript
   For i = 0 To UBound(matrix, 1)
       For j = 0 To UBound(matrix, 2)
           ' 访问数组元素 matrix(i, j)
           ' ...
       Next
   Next
   ```

   可以使用嵌套的循环语句（如 `For` 循环）遍历多维数组中的所有元素。外层循环控制第一个索引，内层循环控制第二个索引。可以根据数组的维度嵌套更多的循环。

多维数组允许您在同一个变量中存储和操作多个维度的数据。它们在处理矩阵、表格、立方体等需要多个维度的数据时非常有用。

#### 集合
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，集合（Collection）是一种用于存储和管理一组相关对象的容器。集合允许您使用一个键来引用存储的对象，从而方便地进行查找、添加、删除和遍历操作。以下是在VBS中使用集合的基本操作方法：

1. 声明和创建集合：
   ```vbscript
   Dim coll              ' 声明一个集合
   Set coll = New Collection
   ```

   在声明集合时，需要使用 `Set` 关键字创建集合对象。

2. 添加对象到集合：
   ```vbscript
   coll.Add object, key
   ```

   使用 `Add` 方法可以将对象添加到集合中，并为对象指定一个唯一的键（可选）。键用于引用和查找特定的对象。如果未提供键，则集合会为对象生成一个默认的键。

3. 访问和操作集合中的对象：
   ```vbscript
   obj = coll(key)         ' 通过键访问对象
   coll.Remove key         ' 根据键删除对象
   coll.RemoveAll          ' 删除集合中的所有对象

   For Each obj In coll    ' 遍历集合中的所有对象
       ' 对每个对象执行操作...
   Next
   ```

   使用集合的键可以轻松地访问和操作集合中的对象。使用 `Remove` 方法可以根据键从集合中删除对象。使用 `RemoveAll` 方法可以删除集合中的所有对象。使用 `For Each` 循环可以遍历集合中的所有对象。

4. 集合的 Count 属性：
   ```vbscript
   count = coll.Count      ' 获取集合中的对象数量
   ```

   使用 `Count` 属性可以获取集合中的对象数量。

集合提供了一种便捷的方式来组织和操作相关对象。它们特别适用于需要动态添加和删除对象的场景。

请注意，VBS的集合是基于零的索引，这意味着索引从 1 开始。当通过键访问对象时，如 `coll(key)`，键也可以是一个数字。

#### 字典
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，字典（Dictionary）是一种用于存储和管理键/值对的数据结构。字典允许您使用键来引用存储的值，从而方便地进行查找、添加、删除和遍历操作。以下是在VBS中使用字典的基本操作方法：

1. 创建和声明字典：
   ```vbscript
   Dim dict              ' 声明一个字典
   Set dict = CreateObject("Scripting.Dictionary")
   ```

   在声明字典时，需要使用 `CreateObject` 函数创建字典对象。

2. 添加键/值对到字典：
   ```vbscript
   dict.Add key, value
   ```

   使用 `Add` 方法可以将键/值对添加到字典中。键用于引用和查找特定的值。

3. 访问和操作字典中的值：
   ```vbscript
   value = dict(key)          ' 通过键访问值
   dict.Remove key            ' 根据键删除键/值对
   dict.RemoveAll             ' 删除字典中的所有键/值对

   For Each key In dict       ' 遍历字典中的所有键
       value = dict(key)      ' 通过键访问对应的值
       ' 对每个键/值对执行操作...
   Next
   ```

   使用字典的键可以轻松地访问和操作字典中的值。使用 `Remove` 方法可以根据键从字典中删除键/值对。使用 `RemoveAll` 方法可以删除字典中的所有键/值对。使用 `For Each` 循环可以遍历字典中的所有键。

4. 字典的 Count 属性：
   ```vbscript
   count = dict.Count         ' 获取字典中的键/值对数量
   ```

   使用 `Count` 属性可以获取字典中的键/值对数量。

字典提供了一种方便的方式来组织和访问键/值对数据。它们特别适用于需要通过键快速查找和访问值的场景。

请注意，VBS的字典是无序的，即字典中的键/值对没有固定的顺序。

## 运算符
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，有多种运算符用于执行不同类型的操作。以下是VBS中的所有运算符分类和示例：

**1. 算术运算符：**
   - `+`：加法运算符。例如：`a + b` 表示将变量 a 和 b 相加。
   - `-`：减法运算符。例如：`a - b` 表示从变量 a 中减去变量 b 的值。
   - `*`：乘法运算符。例如：`a * b` 表示将变量 a 和 b 相乘。
   - `/`：除法运算符。例如：`a / b` 表示将变量 a 除以变量 b。
   - `\`：整数除法运算符。例如：`a \ b` 表示对变量 a 进行整数除以变量 b。
   - `%`：取模运算符。例如：`a Mod b` 表示取变量 a 除以变量 b 的余数。
   - `^`：幂运算符。例如：`a ^ b` 表示将变量 a 的值提升到变量 b 的幂次方。

**2. 比较运算符：**
   - `=`：等于运算符。例如：`a = b` 表示检查变量 a 和 b 是否相等。
   - `<>` 或 `<>`：不等于运算符。例如：`a <> b` 表示检查变量 a 和 b 是否不相等。
   - `>`：大于运算符。例如：`a > b` 表示检查变量 a 是否大于变量 b。
   - `<`：小于运算符。例如：`a < b` 表示检查变量 a 是否小于变量 b。
   - `>=`：大于等于运算符。例如：`a >= b` 表示检查变量 a 是否大于或等于变量 b。
   - `<=`：小于等于运算符。例如：`a <= b` 表示检查变量 a 是否小于或等于变量 b。

**3. 逻辑运算符：**
   - `And`：逻辑与运算符。例如：`a And b` 表示检查变量 a 和变量 b 是否都为 True。
   - `Or`：逻辑或运算符。例如：`a Or b` 表示检查变量 a 和变量 b 是否至少有一个为 True。
   - `Not`：逻辑非运算符。例如：`Not a` 表示取反变量 a 的值。

**4. 位运算符：**
   - `And`：位与运算符。例如：`a And b` 表示对变量 a 和变量 b 执行位与操作。
   - `Or`：位或运算符。例如：`a Or b` 表示对变量 a 和变量 b 执行位或操作。
   - `Xor`：位异或运算符。例如：`a Xor b` 表示对变量 a 和变量 b 执行位异或操作。
   - `Not`：位非运算符。例如：`Not a` 表示对变量 a 执行位非操作。
   - `<<`：左位移运算符。例如：`a << b` 表示将变量 a 的位向左移动 b 位。
   - `>>`：右位移运算符。例如：`a >> b` 表示将变量 a 的位向右移动 b 位。

**5. 字符串连接运算符：**
   - `&`：字符串连接运算符。例如：`str1 & str2` 表示将两个字符串 str1 和 str2 进行连接。

这些运算符可用于执行各种算术、比较、逻辑、位和字符串操作。您可以根据需要选择适当的运算符来实现所需的功能。

## 分支语句
[开头](#vbs帮助文档)
1. **if**
在VBS（Visual Basic Scripting）中，您可以使用 `If` 语句来根据条件执行不同的代码块。`If` 语句的基本语法如下：

```vbscript
If condition Then
    ' 如果条件为真，则执行这里的代码块
End If
```

如果条件 `condition` 为真，则执行 `Then` 代码块中的语句。如果条件为假，则会跳过 `Then` 代码块。

您还可以使用 `Else` 关键字来在条件为假时执行另一段代码块。例如：

```vbscript
If condition Then
    ' 如果条件为真，则执行这里的代码块
Else
    ' 如果条件为假，则执行这里的代码块
End If
```

以下是一个计算BMI（Body Mass Index，体重指数）的示例，演示了如何在VBS中使用 `If` 语句：

```vbscript
Dim weight, height
weight = 70  ' 单位：kg
height = 1.75  ' 单位：m

Dim bmi
bmi = weight / (height * height)

If bmi < 18.5 Then
    Wscript.Echo "BMI is underweight."
ElseIf bmi >= 18.5 And bmi < 25 Then
    Wscript.Echo "BMI is normal weight."
ElseIf bmi >= 25 And bmi < 30 Then
    Wscript.Echo "BMI is overweight."
Else
    Wscript.Echo "BMI is obese."
End If
```

在上述示例中，根据计算得到的BMI的值，使用多个 `If` 语句和 `ElseIf` 关键字来判断BMI的范围并输出相应的结果。根据您的需求，可以编写不同的条件判断逻辑。

2. **select**
在VBS（Visual Basic Scripting）中，您可以使用 `Select Case` 语句根据表达式的值执行不同的代码块。`Select Case` 语句的基本语法如下：

```vbscript
Select Case expression
    Case value1
        ' 如果 expression 的值等于 value1，则执行这里的代码块
    Case value2
        ' 如果 expression 的值等于 value2，则执行这里的代码块
    ...
    Case Else
        ' 如果 expression 的值都不匹配上述情况，则执行这里的代码块
End Select
```

根据表达式 `expression` 的值，选择匹配的 `Case` 分支执行相应的代码块。`Case` 分支可以是具体的值，也可以是表达式。`Case Else` 是可选的，用于处理所有其他情况。

以下是一个根据星期几输出不同信息的示例，演示了如何在VBS中使用 `Select Case` 语句：

```vbscript
Dim day
day = "Monday"

Select Case day
    Case "Monday"
        Wscript.Echo "It's Monday. Start of the week."
    Case "Tuesday"
        Wscript.Echo "It's Tuesday. Second day of the week."
    Case "Wednesday"
        Wscript.Echo "It's Wednesday. Middle of the week."
    Case "Thursday"
        Wscript.Echo "It's Thursday. Fourth day of the week."
    Case "Friday"
        Wscript.Echo "It's Friday. Last working day of the week."
    Case "Saturday", "Sunday"
        Wscript.Echo "It's a weekend day."
    Case Else
        Wscript.Echo "Invalid day."
End Select
```

在上述示例中，根据变量 `day` 的值，使用 `Select Case` 语句判断星期几，并输出相应的信息。

您可以根据您的需求，在 `Select Case` 语句中添加更多的 `Case` 分支来处理不同的情况。

## 循环语句
[开头](#vbs帮助文档)
1. **for**
   在VBS（Visual Basic Scripting）中，`For` 循环是一种常用的循环语句，用于按照指定的条件重复执行代码块。`For` 循环语句的基本语法如下：

```vbscript
For counter = start To end [Step step]
    ' 循环执行的代码块
Next
```

在 `For` 循环中，`counter` 是一个变量，它从 `start` 值开始递增或递减，直到达到或超过 `end` 值为止。`step` 是用于指定递增或递减的步长，默认情况下为 1。

以下是一个计算 1 到 5 的和的示例，演示了如何在 VBS 中使用 `For` 循环：

```vbscript
Dim sum
sum = 0

For i = 1 To 5
    sum = sum + i
Next

Wscript.Echo "Sum: " & sum
```

在上述示例中，`For` 循环从 1 开始递增，直到达到 5 结束。在每次循环中，将 `i` 的值加到 `sum` 变量中。最后，输出累加的结果。

您还可以使用 `Step` 关键字指定递增或递减的步长。例如，要按 2 的步长递增，可以将 `Step` 设置为 2：

```vbscript
For i = 1 To 10 Step 2
    Wscript.Echo i
Next
```

在上述示例中，`i` 的值将从 1 开始，每次递增 2，直到达到或超过 10。

除了 `To` 关键字之外，您还可以使用 `Until` 关键字来指定循环的条件。例如：

```vbscript
For i = 10 Until i < 0 Step -1
    Wscript.Echo i
Next
```

在上述示例中，`i` 的值从 10 开始递减，每次递减 1，直到 `i` 小于 0。

使用 `Exit For` 语句可以提前退出 `For` 循环，以满足某个条件时停止循环执行。

2. **while**
   在VBS（Visual Basic Scripting）中，`While` 循环是一种常用的循环语句，用于根据条件重复执行一段代码块。`While` 循环的基本语法如下：

```vbscript
While condition
    ' 循环执行的代码块
Wend
```

在 `While` 循环中，只要条件 `condition` 为真，就会重复执行代码块。每次循环执行之前，会检查条件的真假。

以下是一个输出 1 到 5 的示例，演示了如何在 VBS 中使用 `While` 循环：

```vbscript
Dim i
i = 1

While i <= 5
    Wscript.Echo i
    i = i + 1
Wend
```

在上述示例中，使用 `While` 循环打印从 1 到 5 的数字。`i` 的初始值是 1，然后在每次循环中递增 1，直到达到或超过 5。

您还可以使用 `Exit While` 语句来提前退出 `While` 循环，以满足某个条件时停止循环执行。

另外，如果您希望先执行一次循环，然后再检查条件，可以使用 `Do While` 循环：

```vbscript
Dim i
i = 1

Do While i <= 5
    Wscript.Echo i
    i = i + 1
Loop
```

在上述示例中，`Do While` 循环先执行一次代码块，然后再检查条件，如果条件为真，则重复执行代码块。

3. **do while**
在VBS（Visual Basic Scripting）中，`Do While` 循环是一种常用的循环语句，用于根据条件重复执行一段代码块。`Do While` 循环的基本语法如下：

```vbscript
Do While condition
    ' 循环执行的代码块
Loop
```

在 `Do While` 循环中，先执行一次代码块，然后检查条件的真假。只要条件 `condition` 为真，就会重复执行代码块。

以下是一个输出 1 到 5 的示例，演示了如何在 VBS 中使用 `Do While` 循环：

```vbscript
Dim i
i = 1

Do While i <= 5
    Wscript.Echo i
    i = i + 1
Loop
```

在上述示例中，使用 `Do While` 循环打印从 1 到 5 的数字。`i` 的初始值是 1，先执行一次输出数字的代码块，然后在每次循环中递增 1，直到达到或超过 5。

您还可以使用 `Exit Do` 语句来提前退出 `Do While` 循环，以满足某个条件时停止循环执行。

另外，如果您希望先检查条件，然后再执行一次代码块，可以使用 `Do Until` 循环：

```vbscript
Dim i
i = 1

Do Until i > 5
    Wscript.Echo i
    i = i + 1
Loop
```

在上述示例中，`Do Until` 循环先检查条件，如果条件为假，则重复执行代码块。

4. **do until**
在VBS（Visual Basic Scripting）中，`Do Until` 循环是一种常用的循环语句，用于在条件为假时重复执行一段代码块。`Do Until` 循环的基本语法如下：

```vbscript
Do Until condition
    ' 循环执行的代码块
Loop
```

在 `Do Until` 循环中，先执行一次代码块，然后检查条件的真假。只要条件 `condition` 为假，就会重复执行代码块。

以下是一个输出 1 到 5 的示例，演示了如何在 VBS 中使用 `Do Until` 循环：

```vbscript
Dim i
i = 1

Do Until i > 5
    Wscript.Echo i
    i = i + 1
Loop
```

在上述示例中，使用 `Do Until` 循环打印从 1 到 5 的数字。`i` 的初始值是 1，先执行一次输出数字的代码块，然后在每次循环中递增 1，直到 `i` 大于 5。

与 `Do While` 循环类似，您也可以使用 `Exit Do` 语句来提前退出 `Do Until` 循环，以满足某个条件时停止循环执行。

需要注意的是，`Do Until` 循环会在条件为真时停止执行，与 `While` 和 `Do While` 循环的条件判断是相反的。

## goto语句
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，`GoTo` 语句用于无条件跳转到程序中的指定标签位置。它是一种流程控制语句，用于修改程序的执行顺序。

`GoTo` 语句的基本语法如下：

```vbscript
GoTo label
```

其中，`label` 是标识符，表示跳转目标的标签。

下面是一个使用 `GoTo` 语句的示例：

```vbscript
Dim i
i = 1

Start:
    WScript.Echo i
    
    i = i + 1
    If i <= 5 Then
        GoTo Start
    End If

Finish:
    WScript.Echo "Done"
```

在上述示例中，使用 `GoTo` 语句实现了一个简单的循环。输出从 1 到 5 的数字，然后跳转到标签 `Finish`，输出 "Done"。

需要注意的是，滥用 `GoTo` 语句可能导致不易阅读、理解和维护的代码。在大多数情况下，可以通过其他的循环语句（如 `For`、`While`、`Do While` 等）或条件语句（如 `If`、`Select Case`）来实现逻辑控制，而避免使用 `GoTo`。

## 函数
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，函数（Function）是一种特殊的代码块，用于执行特定的任务并返回一个值。函数可以接受参数（可选）并在执行完任务后返回一个结果。

以下是一个函数的基本语法：

```vbscript
Function functionName([parameter1, parameter2, ...])
    ' 函数执行的代码块
    functionName = returnValue
End Function
```

在上述语法中：

- `functionName` 是函数的名称，可根据需要自定义。
- `parameter1, parameter2, ...` 是函数的参数列表，可以包含零个或多个参数。
- `returnValue` 是函数执行完毕后返回的值。

以下是一个示例，演示了如何在 VBS 中定义和使用函数：

```vbscript
Function AddNumbers(num1, num2)
    Dim sum
    sum = num1 + num2
    AddNumbers = sum
End Function

Dim result
result = AddNumbers(3, 5)
WScript.Echo result
```

在上述示例中，我们定义了一个名为 `AddNumbers` 的函数，该函数接受两个参数（`num1` 和 `num2`），并返回它们的和。然后我们调用这个函数，并将返回的结果保存在 `result` 变量中，并通过 `WScript.Echo` 输出结果。

在 VBS 中，函数可以接受任意类型的参数（包括字符串、数字、布尔值等），并返回任意类型的值。

除了函数之外，VBS 中还有子过程（Subroutine），子过程类似于函数，但不返回任何值。它们用于执行一系列操作而不返回结果。

## 子过程
[开头](#vbs帮助文档)
在VBS（Visual Basic Scripting）中，子过程（Subroutine）是一种特殊的代码块，用于执行一系列操作。与函数不同，子过程不返回任何值。

以下是一个子过程的基本语法：

```vbscript
Sub subroutineName([parameter1, parameter2, ...])
    ' 子过程执行的代码块
End Sub
```

在上述语法中：

- `subroutineName` 是子过程的名称，可根据需要自定义。
- `parameter1, parameter2, ...` 是子过程的参数列表，可以包含零个或多个参数。

以下是一个示例，演示了如何在 VBS 中定义和使用子过程：

```vbscript
Sub PrintMessage(message)
    WScript.Echo message
End Sub

PrintMessage "Hello, World!"
```

在上述示例中，我们定义了一个名为 `PrintMessage` 的子过程，该子过程接受一个参数（`message`）并通过 `WScript.Echo` 输出该消息。然后我们调用这个子过程，并传递了一个字符串参数 `"Hello, World!"`。

与函数类似，VBS 中的子过程也可以接受任意类型的参数（包括字符串、数字、布尔值等），并在其中执行一系列操作。但不像函数，子过程不返回任何值。

使用子过程可以提高代码的可维护性和复用性，尤其是当需要在多个地方执行相同的一系列操作时。

## 源文件与多文件编程
[开头](#vbs帮助文档)
VBS（Visual Basic Scripting）源文件通常使用.vbs文件扩展名，并且每个.vbs文件通常包含一段完整的VBS代码。

在VBS中进行多文件编程时，可以将代码分布在多个文件中，并通过其他文件引用和调用这些代码。以下是一个示例，演示如何在VBS中进行多文件编程：

1. 创建主文件（例如main.vbs）来调用其他文件：

```vbscript
' main.vbs

' 调用其他文件
Call ExecuteScript("file1.vbs")

' 示例函数
Sub HelloWorld()
    WScript.Echo "Hello, World!"
End Sub

' 调用VBS脚本文件
Sub ExecuteScript(filePath)
    Dim shell
    Set shell = CreateObject("WScript.Shell")
    shell.Run "cscript //nologo " & filePath, 1, True
End Sub
```

在主文件中，我们使用`Call ExecuteScript`语句调用了其他文件（file1.vbs）。这个示例使用了`ExecuteScript`子过程来执行独立的.vbs脚本文件。

2. 创建其他文件（例如file1.vbs）来定义和执行特定的功能：

```vbscript
' file1.vbs

Call GreetUser("John")

' 示例函数
Sub GreetUser(name)
    WScript.Echo "Hello, " & name & "!"
End Sub
```

在其他文件（file1.vbs）中，我们定义了一个`GreetUser`子过程，并在该文件中调用了`GreetUser`子过程。

通过将代码分布在多个文件中，你可以更好地组织和管理代码，使代码更易于理解和维护。在需要使用特定功能时，只需在主文件中调用相应的文件即可。

请注意，在运行VBS脚本之前，请确保你的系统已安装Visual Basic Scripting支持，并正确配置脚本的文件路径。使用上述示例代码时，确保主文件（main.vbs）和其他文件（例如file1.vbs）位于相同的目录下。

## 类与对象
[开头](#vbs帮助文档)
### 类的创建和使用
在 VBS（Visual Basic Scripting）中，类是一种蓝图或模板，用于创建对象。对象是类的实例，它们具有类定义的属性和方法。以下是关于 VBS 类与对象的一些重要概念：

1. 类的定义：可以使用 `Class...End Class` 语句来定义一个类。在类的定义中，可以声明类的属性（Attributes）和方法（Methods）。类还可以定义构造函数（Constructor）和析构函数（Destructor）。以下是一个示例：

```vbscript
Class Person
    Public FirstName As String
    Public LastName As String
    
    Public Sub SayHello()
        WScript.Echo "Hello, my name is " & FirstName & " " & LastName
    End Sub
End Class
```

在上述示例中，我们定义了一个名为 `Person` 的类。它具有两个公共属性 `FirstName` 和 `LastName`，以及一个公共方法 `SayHello`。这个类表示一个人，可以设置姓名并打招呼。

2. 对象的创建：要创建一个类的对象，可以使用 `New` 关键字。以下是一个示例：

```vbscript
Dim p ' 定义对象变量
Set p = New Person ' 创建 Person 对象

p.FirstName = "John" ' 设置对象的属性值
p.LastName = "Doe"
p.SayHello() ' 调用对象的方法
```

在上述示例中，我们创建了一个 `p` 对象作为 `Person` 类的实例。我们可以通过对象变量 `p` 访问类的属性和方法。在示例中，我们设置了对象的 `FirstName` 和 `LastName` 属性，并调用了 `SayHello` 方法来打招呼。

3. 属性和方法的访问：对于对象的属性，可以使用点操作符 `.` 来访问和修改属性的值。对于对象的方法，则可以使用点操作符和括号来调用方法。以下是一个示例：

```vbscript
p.FirstName = "John" ' 访问对象的属性
WScript.Echo p.FirstName

p.SayHello() ' 调用对象的方法
```

在上述示例中，我们通过点操作符来访问和设置对象的属性。然后，我们可以使用点操作符和括号来调用对象的方法。

通过类和对象的使用，我们可以根据需要创建和操作相应的实例。类提供了表示特定类型的数据和相关操作的模板，对象是根据类定义创建的实际实例。通过对象的属性和方法，我们可以操作和访问对象的数据以及执行相应的操作。

### 构造函数和析构函数
[开头](#vbs帮助文档)
在 VBS（Visual Basic Scripting）中，类可以包括构造函数（Constructor）和析构函数（Destructor）来进行对象的初始化和清理工作。

构造函数是在创建类的对象时自动调用的特殊方法。它用于执行对象的初始化操作，例如设置属性的初始值或执行其他必要的步骤。构造函数的名称与类的名称相同，而且没有返回值。要定义构造函数，可以在类中使用 `Sub New...End Sub` 语句。以下是一个示例：

```vbscript
Class Person
    Public FirstName As String
    Public LastName As String
    
    Public Sub New(first As String, last As String)
        FirstName = first
        LastName = last
        WScript.Echo "Person object created: " & FirstName & " " & LastName
    End Sub
    
    Public Sub SayHello()
        WScript.Echo "Hello, my name is " & FirstName & " " & LastName
    End Sub
End Class

Dim p
Set p = New Person("John", "Doe")
p.SayHello()
```

在上述示例中，我们定义了一个名为 `Person` 的类，并在类中定义了一个构造函数 `New`。构造函数接受两个参数 `first` 和 `last`，用于设置对象的 `FirstName` 和 `LastName` 属性。在构造函数中，我们输出一条创建对象的消息。然后，我们创建了一个 `p` 对象，并传递参数 `"John"` 和 `"Doe"` 给构造函数进行初始化。最后，我们调用对象的 `SayHello` 方法。

析构函数是在对象被销毁时自动调用的特殊方法。它用于执行对象的清理操作，例如释放资源或执行其他必要的清理步骤。析构函数的名称与类的名称相同，但在名称前面加上一个下划线 `_`。要定义析构函数，可以在类中使用 `Sub Class_Terminate...End Sub` 语句。以下是一个示例：

```vbscript
Class Person
    Public FirstName As String
    Public LastName As String
    
    Public Sub New(first As String, last As String)
        FirstName = first
        LastName = last
        WScript.Echo "Person object created: " & FirstName & " " & LastName
    End Sub
    
    Public Sub Class_Terminate()
        WScript.Echo "Person object destroyed: " & FirstName & " " & LastName
    End Sub
    
    Public Sub SayHello()
        WScript.Echo "Hello, my name is " & FirstName & " " & LastName
    End Sub
End Class

Set p = New Person("John", "Doe")
p.SayHello()
Set p = Nothing ' 销毁对象
```

在上述示例中，我们定义了一个名为 `Person` 的类，并添加了一个析构函数 `Class_Terminate`。析构函数在对象被销毁时自动调用。在析构函数中，我们输出一条销毁对象的消息。然后，我们创建了一个 `p` 对象，并执行一些操作。最后，我们将对象设置为 `Nothing`，从而销毁对象并触发析构函数。

构造函数和析构函数在类中提供了管理对象生命周期的能力。通过构造函数，可以在对象创建时进行初始化操作。通过析构函数，可以在对象销毁时进行必要的清理操作。使用构造函数和析构函数可以更好地控制对象的行为和资源的管理。

### 对象数组
[开头](#vbs帮助文档)
在 VBS（Visual Basic Scripting）中，可以创建对象数组，用于存储多个对象的实例。对象数组允许在同一个数组中存储多个相同类型的对象，并对它们进行操作。

以下是创建和操作对象数组的示例：

```vbscript
Class Person
    Public FirstName As String
    Public LastName As String
    
    Private Sub Class_Initialize()
        FirstName = ""
        LastName = ""
    End Sub
    
    Public Sub SetName(first As String, last As String)
        FirstName = first
        LastName = last
    End Sub
    
    Public Sub ShowName()
        WScript.Echo "Name: " & FirstName & " " & LastName
    End Sub
End Class

Dim people(2) ' 创建 Person 对象数组
Set people(0) = New Person
Set people(1) = New Person
Set people(2) = New Person

people(0).SetName "John", "Doe"
people(1).SetName "Jane", "Smith"
people(2).SetName "Mike", "Johnson"

For Each person In people
    person.ShowName ' 对每个对象调用方法
Next
```

在上述示例中，我们首先定义了一个 `Person` 类，它有 `FirstName` 和 `LastName` 属性，以及 `SetName` 和 `ShowName` 方法。然后，我们创建了一个包含三个元素的对象数组 `people`。通过使用 `Set` 关键字，我们将 `Person` 对象的实例分配给数组的元素。

接下来，我们为每个对象调用 `SetName` 方法来设置姓名。最后，我们使用 `For Each` 语句遍历对象数组，对每个对象调用 `ShowName` 方法来显示姓名。

通过对象数组，我们可以在 VBS 中方便地存储和操作多个对象的实例。我们可以使用循环结构（如 `For Each`）遍历数组，并对每个对象执行相应的操作。这种灵活性允许我们有效地处理多个对象，并在需要时对其进行批量处理。

### 类继承
[开头](#vbs帮助文档)
在 VBS（Visual Basic Scripting）中，可以使用类继承创建一个类继承另一个类的属性和方法。类继承是一种面向对象编程的基本概念，它允许通过继承现有类的特性来创建新的类。

要实现类继承，可以使用关键字 `Class` 后面的 `Inherits` 来指定要继承的父类。子类将继承父类的属性和方法，并可以在子类中进行扩展或重写。

以下是一个使用类继承的示例：

```vbscript
Class Animal
    Public Name As String
    Public Age As Integer
    
    Public Sub Eat()
        WScript.Echo Name & " is eating."
    End Sub
End Class

Class Dog
    Inherits Animal
    
    Public Sub Bark()
        WScript.Echo Name & " is barking."
    End Sub
End Class

Dim myDog
Set myDog = New Dog
myDog.Name = "Buddy"
myDog.Age = 3

myDog.Eat()
myDog.Bark()
```

在上述示例中，我们首先定义了一个名为 `Animal` 的基类，它有属性 `Name` 和 `Age`，以及方法 `Eat`。然后，我们定义了一个名为 `Dog` 的子类，并使用 `Inherits Animal` 指定它继承自 `Animal` 类。子类 `Dog` 添加了一个额外的方法 `Bark`。

我们创建一个 `myDog` 对象，它是 `Dog` 类的实例。我们可以访问继承自父类的属性和方法，例如 `Name` 和 `Age` 属性，以及 `Eat` 方法。此外，我们还可以使用子类独有的方法 `Bark`。

通过类继承，我们可以构建更具层次结构和灵活性的代码。子类可以继承和扩展父类的功能，从而减少代码的重复和冗余，并使代码更易于维护和扩展。

## 异常处理
[开头](#vbs帮助文档)
在 VBS（Visual Basic Scripting）中，可以使用异常处理机制来捕获和处理运行时出现的异常。异常处理允许在发生异常时采取适当的措施，而不会导致脚本终止或产生未处理的错误。

VBS使用 `On Error` 语句来控制异常处理。以下是一些常用的异常处理技术：

1. `On Error Resume Next`: 当使用 `On Error Resume Next` 语句时，脚本会继续执行下一个语句，而不是在产生错误时停止执行。在这种情况下，需要使用 `Err` 对象来检查错误并采取适当的措施。

```vbscript
On Error Resume Next

' 可能会引发错误的代码
' ...

If Err.Number <> 0 Then
    ' 处理或记录错误
    ' ...
End If

' 恢复错误处理行为
On Error GoTo 0
```

2. `On Error GoTo` 和 `Err.Raise`: 使用 `On Error GoTo` 可以指定发生异常时要跳转到的错误处理代码行。当使用 `Err.Raise` 语句抛出异常时，脚本会跳转到指定的错误处理代码块。

```vbscript
On Error GoTo ErrorHandler

' 可能会引发错误的代码
' ...

Exit Sub ' 如果没有错误，可退出错误处理

ErrorHandler:
    ' 处理或记录错误
    ' 可以使用 Err 对象访问错误信息
    ' ...
    Resume Next ' 继续执行下一个语句

' 恢复错误处理行为
On Error GoTo 0
```

3. 使用 `Err` 对象：`Err` 对象是一个内置对象，提供了有关最近一次发生的错误的信息，例如错误号（`Number`）和错误描述（`Description`）等。可以通过检查 `Err` 对象的属性来进行错误处理。

```vbscript
On Error Resume Next

' 可能会引发错误的代码
' ...

If Err.Number <> 0 Then
    ' 处理或记录错误
    ' 可以使用 Err 对象访问错误信息
    MsgBox "Error Number: " & Err.Number & vbCrLf & "Description: " & Err.Description
End If

' 恢复错误处理行为
On Error GoTo 0
```

使用异常处理机制可以更好地控制和处理脚本中的异常情况，帮助保证程序的稳定性和可靠性。根据实际需要，可以选择适合自己的异常处理技术。

