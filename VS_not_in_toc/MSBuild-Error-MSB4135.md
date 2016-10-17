---
title: "MSBuild Error MSB4135"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9192f772-ad13-42f7-b53f-c5e31846fa5f
caps.latest.revision: 9
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
# MSBuild Error MSB4135
**MSB4135: Error reading the toolset information from the registry key "'<key\>'" or a subkey. '<key\>'**  
  
 The custom Toolset information defined in the registry could not be read.  
  
### To correct this error  
  
-   If you have defined a custom Toolset in the registry, make sure that it is in valid registry format, that is has the correct `ToolsVersion` name and that the correct `MSBuildBinPath` or `MSBuildToolsPath` value.  
  
## See Also  
 [Standard and Custom Toolset Configurations](../VS_IDE/Standard-and-Custom-Toolset-Configurations.md)   
 [Project Element (MSBuild)](../VS_IDE/Project-Element--MSBuild-.md)   
 [Additional Resources](../VS_IDE/Additional-MSBuild-Resources.md)