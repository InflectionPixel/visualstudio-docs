---
title: "IDiaSession::findChildren"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5d19046f-f668-4aa9-8788-95cda9a98997
caps.latest.revision: 10
manager: ghogen
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
# IDiaSession::findChildren
Retrieves all children of a specified parent identifier that match the name and symbol type.  
  
## Syntax  
  
```cpp#  
HRESULT findChildren (   
   IDiaSymbol*       parent,  
   SymTagEnum        symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### Parameters  
 `parent`  
 [in] An [IDiaSymbol](../VS_debugger/IDiaSymbol.md) object representing the parent. If this parent symbol is a function, module, or block, then its lexical children are returned in `ppResult`. If the parent symbol is a type, then its class children are returned. If this parameter is `NULL`, then `symtag` must be set to `SymTagExe` or `SymTagNull`, which returns the global scope (.exe file).  
  
 `symtag`  
 [in] Specifies the symbol tag of the children to be retrieved. Values are taken from the [SymTagEnum Enumeration](../VS_debugger/SymTagEnum.md) enumeration. Set to `SymTagNull` to retrieve all children.  
  
 `name`  
 [in] Specifies the name of the children to be retrieved. Set to `NULL` for all children to be retrieved.  
  
 `compareFlags`  
 [in] Specifies the comparison options applied to name matching. Values from the [NameSearchOptions Enumeration](../VS_debugger/NameSearchOptions.md) enumeration can be used alone or in combination.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumSymbols](../VS_debugger/IDiaEnumSymbols.md) object that contains the list of child symbols retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Example  
 The following example shows how to find local variables of function `pFunc` that match name `szVarName`.  
  
```cpp#  
IDiaEnumSymbols* pEnum;  
pSession->findChildren( pFunc, SymTagData, szVarName, nsCaseSensitive, &pEnum );  
```  
  
## See Also  
 [Overview](../VS_debugger/Overview--Debug-Interface-Access-SDK-.md)   
 [IDiaEnumSymbols](../VS_debugger/IDiaEnumSymbols.md)   
 [IDiaSession](../VS_debugger/IDiaSession.md)   
 [IDiaSymbol](../VS_debugger/IDiaSymbol.md)   
 [NameSearchOptions Enumeration](../VS_debugger/NameSearchOptions.md)   
 [SymTagEnum Enumeration](../VS_debugger/SymTagEnum.md)