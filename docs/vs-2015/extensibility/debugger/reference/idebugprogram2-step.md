---
title: "IDebugProgram2::Step | Microsoft Docs"
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
  - "IDebugProgram2::Step"
helpviewer_keywords: 
  - "IDebugProgram2::Step"
ms.assetid: e4c2ffce-9810-4088-8162-eac9ef04f2a9
caps.latest.revision: 17
ms.author: "gregvanl"
manager: "ghogen"
---
# IDebugProgram2::Step
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDebugProgram2::Step](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprogram2-step).  
  
Performs a step.  
  
> [!NOTE]
>  This method is deprecated. Use the [Step](../../../extensibility/debugger/reference/idebugprocess3-step.md) method instead.  
  
## Syntax  
  
```cpp#  
HRESULT Step(   
   IDebugThread2*  pThread,  
   STEPKIND        sk,  
   STEPUNIT        step  
);  
```  
  
```csharp  
int Step(   
   IDebugThread2  pThread,  
   enum_STEPKIND  sk,  
   enum_STEPUNIT  step  
);  
```  
  
#### Parameters  
 `pThread`  
 [in] An [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) object that represents the thread being stepped.  
  
 `sk`  
 [in] A value from the [STEPKIND](../../../extensibility/debugger/reference/stepkind.md) enumeration that specifies the kind of step.  
  
 `step`  
 [in] A value from the [STEPUNIT](../../../extensibility/debugger/reference/stepunit.md) enumeration that specifies the unit of step (for example, by statement or instruction).  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 In case there is any thread synchronization or communication between threads, other threads in the program should run when a particular thread is stepping.  
  
> [!WARNING]
>  Do not send a stopping event or an immediate (synchronous) event to [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) while handling this call; otherwise the debugger may hang.  
  
## See Also  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)   
 [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)

