---
title: "Procedure Parameters and Arguments (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "procedures, arguments"
  - "procedures, argument lists"
  - "values, passing to procedures"
  - "arguments [Visual Basic], passing"
  - "procedures, parameters"
  - "Visual Basic code, argument lists"
  - "Visual Basic code, procedures"
  - "parameters, Visual Basic procedures"
  - "parameters, lists"
  - "arguments [Visual Basic], Visual Basic procedures"
  - "arguments [Visual Basic], procedures"
  - "parameter lists"
  - "Visual Basic code, parameter lists"
  - "argument lists"
  - "procedures, parameter lists"
ms.assetid: ff275aff-aa13-40df-bd4c-63486db8c1e9
caps.latest.revision: 21
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Procedure Parameters and Arguments (Visual Basic)
In most cases, a procedure needs some information about the circumstances in which it has been called. A procedure that performs repeated or shared tasks uses different information for each call. This information consists of variables, constants, and expressions that you pass to the procedure when you call it.  
  
 A *parameter* represents a value that the procedure expects you to supply when you call it. The procedure's declaration defines its parameters.  
  
 You can define a procedure with no parameters, one parameter, or more than one. The part of the procedure definition that specifies the parameters is called the *parameter list*.  
  
 An *argument* represents the value you supply to a procedure parameter when you call the procedure. The calling code supplies the arguments when it calls the procedure. The part of the procedure call that specifies the arguments is called the *argument list*.  
  
 The following illustration shows code calling the procedure `safeSquareRoot` from two different places. The first call passes the value of the variable `x` (4.0) to the parameter `number`, and the return value in `root` (2.0) is assigned to the variable `y`. The second call passes the literal value 9.0 to `number`, and assigns the return value (3.0) to variable `z`.  
  
 ![Graphic diagram of passing argument to parameter](../../../visual-basic/language-reference/procedures/media/parametersargue.gif "ParametersArgue")  
Passing an argument to a parameter  
  
 For more information, see [Differences Between Parameters and Arguments](../../../visual-basic/language-reference/procedures/differences-between-parameters-and-arguments.md).  
  
## Parameter Data Type  
 You define a data type for a parameter by using the `As` clause in its declaration. For example, the following function accepts a string and an integer.  
  
 [!code-vb[VbVbcnProcedures#32](../../../visual-basic/language-reference/procedures/codesnippet/VisualBasic/procedure-parameters-and-arguments_1.vb)]  
  
 If the type checking switch ([Option Strict Statement](../../../visual-basic/language-reference/statements/option-strict-statement.md)) is `Off,` the `As` clause is optional, except that if any one parameter uses it, all parameters must use it. If type checking is `On`, the `As` clause is required for all procedure parameters.  
  
 If the calling code expects to supply an argument with a data type different from that of its corresponding parameter, such as `Byte` to a `String` parameter, it must do one of the following:  
  
-   Supply only arguments with data types that widen to the parameter data type;  
  
-   Set `Option Strict Off` to allow implicit narrowing conversions; or  
  
-   Use a conversion keyword to explicitly convert the data type.  
  
### Type Parameters  
 A *generic procedure* also defines one or more *type parameters* in addition to its normal parameters. A generic procedure allows the calling code to pass different data types each time it calls the procedure, so it can tailor the data types to the requirements of each individual call. See [Generic Procedures in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md).  
  
## See Also  
 [Procedures](../../../visual-basic/language-reference/procedures/index.md)   
 [Sub Procedures](../../../visual-basic/language-reference/procedures/sub-procedures.md)   
 [Function Procedures](../../../visual-basic/language-reference/procedures/function-procedures.md)   
 [Property Procedures](../../../visual-basic/language-reference/procedures/property-procedures.md)   
 [Operator Procedures](../../../visual-basic/language-reference/procedures/operator-procedures.md)   
 [How to: Define a Parameter for a Procedure](../../../visual-basic/language-reference/procedures/how-to-define-a-parameter-for-a-procedure.md)   
 [How to: Pass Arguments to a Procedure](../../../visual-basic/language-reference/procedures/how-to-pass-arguments-to-a-procedure.md)   
 [Passing Arguments by Value and by Reference](../../../visual-basic/language-reference/procedures/passing-arguments-by-value-and-by-reference.md)   
 [Procedure Overloading](../../../visual-basic/language-reference/procedures/procedure-overloading.md)   
 [Type Conversions in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)