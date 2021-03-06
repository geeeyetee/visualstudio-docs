---
title: "IDebugProcess2::CauseBreak | Microsoft Docs"
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
  - "IDebugProcess2::CauseBreak"
helpviewer_keywords: 
  - "IDebugProcess2::CauseBreak"
ms.assetid: efda8865-2319-4d53-90bf-6d9d74cd5195
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
---
# IDebugProcess2::CauseBreak
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDebugProcess2::CauseBreak](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprocess2-causebreak).  
  
Requests that the next program that is running code in this process halt and send an [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) event object.  
  
## Syntax  
  
```cpp#  
HRESULT CauseBreak(   
   void  
);  
```  
  
```csharp  
int CauseBreak();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)

