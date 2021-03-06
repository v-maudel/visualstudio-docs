---
title: "Disabling the Visual Studio Debugger for Windows Workflow Foundation (Legacy) | Microsoft Docs"
ms.date: "11/04/2016"
ms.topic: "reference"
helpviewer_keywords: 
  - "workflows, disabling debugger"
  - "debugging workflows, disabling debugger"
  - "workflow debugger, disabling"
ms.assetid: 9da96d0e-f941-4fa9-a1a5-6bab50adfec9
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: 
  - "multiple"
---
# Disabling the Visual Studio Debugger for Windows Workflow Foundation (Legacy)

This topic describes how to disable the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Debugger using the configuration file when building [!INCLUDE[wf](../workflow-designer/includes/wf_md.md)] applications in the legacy Windows Workflow Designer. Use the legacy [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] when you need to target either the [!INCLUDE[netfx35_long](../workflow-designer/includes/netfx35_long_md.md)] or the [!INCLUDE[vstecwinfx](../workflow-designer/includes/vstecwinfx_md.md)].

 By default, the [!INCLUDE[vs_current_long](../misc/includes/vs_current_long_md.md)] Debugger for [!INCLUDE[wf](../workflow-designer/includes/wf_md.md)] is enabled for a host process. To disable workflow debugging, you must explicitly turn it off by adding a "DisableWorkflowDebugging" entry **\<switches>** element in the **\<system.diagnostics>** section of the host configuration file.

 The following example shows how to modify the host configuration file to disable workflow debugging.

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
   <system.diagnostics>
      <switches>
         <add name="DisableWorkflowDebugging" value="true"/>
      </switches>
   </system.diagnostics>
</configuration>
```

## See also

- [Invoking the Visual Studio Debugger for Windows Workflow Foundation (Legacy)](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)
- [Debugging Legacy Workflows](../workflow-designer/debugging-legacy-workflows.md)