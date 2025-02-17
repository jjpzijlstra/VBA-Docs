---
title: TextBox.EventProcPrefix property (Access)
keywords: vbaac10.chm11040
f1_keywords:
- vbaac10.chm11040
ms.prod: access
api_name:
- Access.TextBox.EventProcPrefix
ms.assetid: a8cd7cdc-605b-473c-95b1-9d1736e0ec96
ms.date: 02/21/2019
ms.localizationpriority: medium
---


# TextBox.EventProcPrefix property (Access)

Gets or sets the prefix portion of an event procedure name. Read/write **String**.


## Syntax

_expression_.**EventProcPrefix**

_expression_ A variable that represents a **[TextBox](Access.TextBox.md)** object.


## Remarks

For example, if you have a command button with an event procedure named **Details_Click**, the **EventProcPrefix** property returns the string **Details**.

Microsoft Access adds the prefix portion of an event procedure name to the event name with an underscore character ( _ ).




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]