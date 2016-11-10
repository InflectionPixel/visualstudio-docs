---
title: "Troubleshooting Exceptions: System.NotCancelableException"
ms.custom: na
ms.date: 10/02/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36b82d4b-f075-4af5-993a-3e763a7e254a
caps.latest.revision: 10
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
# Troubleshooting Exceptions: System.NotCancelableException
A `NotCancelableException` is thrown when an attempt is made to cancel an operation that is not cancelable.  
  
## Associated Tips  
 Do not try to cancel the operation.  
 Some operations cannot be canceled and will throw this exception when such an attempt is made. Avoid giving the user an option to cancel the operation in these cases.  
  
## See Also  
 [Use the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)