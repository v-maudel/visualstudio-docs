---
title: "IDebugModuleLoadEvent2::GetModule | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDebugModuleLoadEvent2::GetModule"
helpviewer_keywords: 
  - "IDebugModuleLoadEvent2::GetModule"
ms.assetid: c86482bb-9ce5-4e63-bbe0-969b50169424
caps.latest.revision: 10
author: "gregvanl"
ms.author: "gregvanl"
manager: ghogen
ms.workload: 
  - "vssdk"
---
# IDebugModuleLoadEvent2::GetModule
Gets the module that is being loaded or unloaded.  
  
## Syntax  
  
```cpp  
HRESULT GetModule(   
   IDebugModule2** pModule,  
   BSTR*           pbstrDebugMessage,  
   BOOL*           pbLoad  
);  
```  
  
```csharp  
int GetModule(   
   out IDebugModule2 pModule,  
   ref string        pbstrDebugMessage,  
   ref int           pbLoad  
);  
```  
  
#### Parameters  
 `pModule`  
 [out] Returns an [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) object that represents the module which is loading or unloading.  
  
 `pbstrDebugMessage`  
 [in, out] Returns an optional message describing this event. If this parameter is a null value, no message is requested.  
  
 `pbLoad`  
 [in, out] Nonzero (`TRUE`) if the module is loading and zero (`FALSE`) if the module is unloading. If this parameter is a null value, no status is requested.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugModuleLoadEvent2](../../../extensibility/debugger/reference/idebugmoduleloadevent2.md)   
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)