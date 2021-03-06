---
title: "TaskBody Element (MSBuild) | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "TaskBody element [MSBuild]"
  - "<TaskBody> element [MSBuild]"
ms.assetid: 49d8741b-f1ea-4470-94fd-a1ac27341a6a
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: "ghogen"
---
# TaskBody Element (MSBuild)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [TaskBody Element (MSBuild)](https://docs.microsoft.com/visualstudio/msbuild/taskbody-element-msbuild).  
  
  
Contains the data that is passed to a `UsingTask``TaskFactory`. For more information, see [UsingTask Element (MSBuild)](../msbuild/usingtask-element-msbuild.md).  
  
 \<Project>  
 \<UsingTask>  
 \<TaskBody>  
  
## Syntax  
  
```  
<TaskBody Evaluate="true/false" />  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Evaluate`|Optional Boolean attribute.<br /><br /> If `true`, MSBuild evaluates any inner elements, and expands items and properties before it passes the information to the `TaskFactory` when the task is instantiated.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|Data|The text between the `TaskBody` tags is sent verbatim to the `TaskFactory`.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[UsingTask](../msbuild/usingtask-element-msbuild.md)|Provides a way to register tasks in [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]. There may be zero or more `UsingTask` elements in a project.|  
  
## Example  
 The following example shows how to use the `TaskBody` element with an `Evaluate` attribute.  
  
```  
<UsingTask TaskName="MyTask" AssemblyName="My.Assembly" TaskFactory="MyTaskFactory">  
       <ParameterGroup>  
              <Parameter1 ParameterType="System.String" Required="False" Output="False"/>  
              <Parameter2 ParameterType="System.Int" Required="True" Output="False"/>  
              ...  
</ParameterGroup>  
       <TaskBody Evaluate="true">  
      ... Task factory-specific data ...  
       </TaskBody>  
</UsingTask>  
```  
  
## See Also  
 [Tasks](../msbuild/msbuild-tasks.md)   
 [Task Reference](../msbuild/msbuild-task-reference.md)   
 [Project File Schema Reference](../msbuild/msbuild-project-file-schema-reference.md)



