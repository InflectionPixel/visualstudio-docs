---
title: "Compiler Error CS1675"
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
ms.assetid: add10021-f751-45c7-addc-0f73fa4a267c
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
# Compiler Error CS1675
Enums cannot have type parameters  
  
 To resolve this error, remove the type parameter from the `enum` declaration.  
  
## Example  
 The following sample generates CS1675:  
  
```  
// CS1675.cs  
enum E<T>  // CS1675  
{  
}  
  
class CMain  
{  
    public static void Main()  
    {  
    }  
}  
```