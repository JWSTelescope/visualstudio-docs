---
title: "Compiler Error CS0146"
ms.custom: na
ms.date: 10/02/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2be796e5-da2c-4939-af12-3145cd1828c8
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
# Compiler Error CS0146
Circular base class dependency involving 'class1' and 'class2'  
  
 The inheritance list for a class includes a direct or indirect reference to itself. A class cannot inherit from itself. For more information, see [Inheritance](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0146:  
  
```  
// CS0146.cs  
namespace MyNamespace  
{  
   public interface InterfaceA  
   {  
   }  
  
   public class MyClass : InterfaceA, MyClass2  
   {  
      public void Main()  
      {  
      }  
   }  
  
   public class MyClass2 : MyClass   // CS0146  
   {  
   }  
}  
```