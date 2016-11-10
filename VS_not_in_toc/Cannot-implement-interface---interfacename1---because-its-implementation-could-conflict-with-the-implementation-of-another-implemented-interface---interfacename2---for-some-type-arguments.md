---
title: "Cannot implement interface &#39;&lt;interfacename1&gt;&#39; because its implementation could conflict with the implementation of another implemented interface &#39;&lt;interfacename2&gt;&#39; for some type arguments"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: af1cc688-c8cf-4cb2-a8a9-310f5139fe7b
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
# Cannot implement interface &#39;&lt;interfacename1&gt;&#39; because its implementation could conflict with the implementation of another implemented interface &#39;&lt;interfacename2&gt;&#39; for some type arguments
A class declaration includes an `Implements` statement that specifies two or more interfaces, but at least one of the interfaces is generic and two of the implementations could conflict for certain values of type arguments.  
  
 The following statements can generate this error.  
  
```  
Public Interface iFace1  
    Sub testSub(ByVal arg As String)  
End Interface  
Public Interface iFace2(Of t)  
    Sub testSub(ByVal arg As t)  
End Interface  
Public Class testClass  
    Implements iFace1, iFace2(Of String)  
End Class  
```  
  
 Because `iFace2` is constructed using `String`, `testClass` must implement two versions of `testSub` with identical signatures. Doing so would produce an ambiguity about which version to access.  
  
 **Error ID:** BC32072  
  
### To correct this error  
  
-   Change the type argument supplied to the generic interface so that there is no conflict.  
  
     -or-  
  
-   Remove from the `Implements` statement one of the interfaces resulting in the implementation conflict.  
  
## See Also  
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Interface Statement](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Implements Statement](../Topic/Implements%20Statement.md)   
 [NOT IN BUILD: Implements Keyword and Implements Statement](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)