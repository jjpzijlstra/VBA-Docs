---
title: Font.Italic property (Publisher)
keywords: vbapb10.chm5373968
f1_keywords:
- vbapb10.chm5373968
ms.prod: publisher
api_name:
- Publisher.Font.Italic
ms.assetid: c55c0bfa-a365-86ac-4cfb-f6911dadd0af
ms.date: 06/08/2019
ms.localizationpriority: medium
---


# Font.Italic property (Publisher)

Returns or sets an **[MsoTriState](Office.MsoTriState.md)** constant indicating whether the specified text is formatted as italic. Read/write.


## Syntax

_expression_.**Italic**

_expression_ A variable that represents a **[Font](Publisher.Font.md)** object.


## Return value

MsoTriState


## Remarks

The **Italic** property value can be one of the **MsoTriState** constants declared in the Microsoft Office type library and shown in the following table.

|Constant|Description|
|:-----|:-----|
| **msoFalse**|None of the characters in the range are formatted as italic.|
| **msoTriStateMixed**|A return value indicating a combination of **msoTrue** and **msoFalse** for the specified shape range.|
| **msoTriStateToggle**|A set value that switches between **msoTrue** and **msoFalse**.|
| **msoTrue**|All of the characters in the range are formatted as italic.|

## Example

This example tests all the text in the second story of the active publication, and if it has some text formatted as italic, it sets all the text to italic. If the text is all italic or all not italic, a message is displayed informing the user that there is no mixed italic formatting.

```vb
Sub ItalicStory() 
 
 Dim stf As Font 
 
 Set stf = Application.ActiveDocument.Stories(2).TextRange.Font 
 With stf 
 If .Italic = msoTriStateMixed Then 
 .Italic = msoTrue 
 Else 
 MsgBox "There is no mixed italic formatting in this story." 
 End If 
 End With 
 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]