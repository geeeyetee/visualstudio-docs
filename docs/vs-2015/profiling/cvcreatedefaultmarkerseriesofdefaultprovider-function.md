---
title: "CvCreateDefaultMarkerSeriesOfDefaultProvider Function | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "cvmarkers/CvCreateDefaultMarkerSeriesOfDefaultProvider"
helpviewer_keywords: 
  - "CvCreateDefaultMarkerSeriesOfDefaultProvider method"
ms.assetid: 24eb80f8-8fca-4c47-93b5-bb1eb8ffdffd
caps.latest.revision: 7
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# CvCreateDefaultMarkerSeriesOfDefaultProvider Function
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [CvCreateDefaultMarkerSeriesOfDefaultProvider Function](https://docs.microsoft.com/visualstudio/profiling/cvcreatedefaultmarkerseriesofdefaultprovider-function).  
  
Creates default marker series of a default provider.  
  
## Syntax  
  
```  
HRESULT CvCreateDefaultMarkerSeriesOfDefaultProvider(  
   _Out_ PCV_PROVIDER* ppProvider,  
   _Out_ PCV_MARKERSERIES* ppMarkerSeries  
);  
```  
  
#### Parameters  
 `ppProvider`  
 Address of provider object variable. Address cannot be NULL, the variable can have any value.  
  
 `ppMarkerSeries`  
 Address of marker series object variable. Address cannot be NULL, the variable can have any value.  
  
## Return Value  
 S_OK when both provider and marker series are successfully created or error code in case there were any errors. Use SUCCEEDED/FAILED macros to check for error condition.  
  
## Requirements  
 **Header:** cvmarkers.h  
  
## See Also  
 [C++ Library Reference](../profiling/cpp-library-reference.md)



