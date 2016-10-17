---
title: "Compiler Error CS1935"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d5dda801-fbf3-4340-bfe1-f9409f2d344d
caps.latest.revision: 7
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Compiler Error CS1935
Could not find an implementation of the query pattern for source type 'type'. 'method' not found. Are you missing a reference to 'System.Core.dll' or a using directive for 'System.Linq'?  
  
 The source type in a query must be `IEnumerable`, `IEnumerable<T>`, or a derived type, or a type for which you or someone else has implemented the standard query operators. If the source type is an `IEnumerable` or `IEnumerable<T>`, you must add a reference to system.core.dll and a `using` directive for the System.Linq namespace in order to bring the standard query operator extension methods into scope. Custom implementations of the standard query operators must be brought into scope in the same way, with a `using` directive and, if necessary, a reference to the assembly.  
  
### To correct this error  
  
1.  Add the required using directives and references to the project.  
  
## Example  
 The following code generates CS1935 because the `using` directive for System.Linq is commented out:  
  
```  
// cs1935.cs  
// CS1935  
using System;  
using System.Collections.Generic;  
// using System.Linq;  
  
class Test  
{  
    static int Main()  
    {  
        int[] nums = {0,1,2,3,4,5};  
        IEnumerable<int> e = from n in nums  
                        where n > 3  
                        select n;  
        return 0;  
    }  
}  
```  
  
## See Also  
 [Standard Query Operators Overview](../Topic/Standard%20Query%20Operators%20Overview.md)