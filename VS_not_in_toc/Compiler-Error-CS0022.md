---
title: "Compiler Error CS0022"
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
ms.assetid: 531c3ed2-0d75-4046-8d57-89f79381af8e
caps.latest.revision: 8
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
# Compiler Error CS0022
Wrong number of indices inside [], expected 'number'  
  
 An array-access operation specified the incorrect number of dimensions within the square brackets. For more information, see [Arrays](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0022:  
  
```  
// CS0022.cs  
public class MyClass  
{  
    public static void Main()  
    {  
        int[] a = new int[10];  
        a[0] = 0;     // single-dimension array  
        a[0,1] = 9;   // CS0022, the array does not have two dimensions  
    }  
}  
```