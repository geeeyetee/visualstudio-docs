---
title: "SYMBOL_SEARCH_INFO_FIELDS | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "SYMBOL_SEARCH_INFO_FIELDS"
helpviewer_keywords: 
  - "SYMBOL_SEARCH_INFO_FIELDS enumeration"
ms.assetid: bce35af0-722d-46d4-afa6-eaae598c51ff
caps.latest.revision: 10
ms.author: "gregvanl"
manager: "ghogen"
---
# SYMBOL_SEARCH_INFO_FIELDS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [SYMBOL_SEARCH_INFO_FIELDS](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/symbol-search-info-fields).  
  
Specifies the kind of symbol information to retrieve.  
  
## Syntax  
  
```cpp#  
enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
typedef DWORD SYMBOL_SEARCH_INFO_FIELDS;  
```  
  
```csharp  
public enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
  
```  
  
## Members  
 SSIF_NONE  
 Indicates no flags  
  
 SSIF_VERBOSE_SEARCH_INFO  
 Returns all search paths used for finding symbols  
  
## Remarks  
 These flags are passed as a parameter to the [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md) method to determine the amount of information returned.  
  
> [!NOTE]
>  Currently, only `SSIF_VERBOSE_SEARCH_INFO` is supported, and it must be specified as the `dwFlags` parameter to `IDebugModule3::GetSymbolInfo`. All other values return an error.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md)

