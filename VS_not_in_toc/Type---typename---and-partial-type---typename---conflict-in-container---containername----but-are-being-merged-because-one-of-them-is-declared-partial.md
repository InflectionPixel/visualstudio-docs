---
title: "Type &#39;&lt;typename&gt;&#39; and partial type &#39;&lt;typename&gt;&#39; conflict in container &#39;&lt;containername&gt;&#39;, but are being merged because one of them is declared partial"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c243e70b-ecd5-49ef-a260-a7bb12a4a3b1
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
# Type &#39;&lt;typename&gt;&#39; and partial type &#39;&lt;typename&gt;&#39; conflict in container &#39;&lt;containername&gt;&#39;, but are being merged because one of them is declared partial
A class or structure is appears in multiple definitions in the same container type, and more than one definition is not marked `Partial`.  
  
 You must use the [Partial](../Topic/Partial%20\(Visual%20Basic\).md) keyword on at least one of the multiple definitions of a class or structure, but it is recommended that you use it on all the partial definitions.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../VS_IDE/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40046  
  
### To correct this error  
  
-   Use the [Partial](../Topic/Partial%20\(Visual%20Basic\).md) keyword on every partial definition of the class or structure.  
  
## See Also  
 [Partial](../Topic/Partial%20\(Visual%20Basic\).md)