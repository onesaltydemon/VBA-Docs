---
title: Report.PrintCount property (Access)
keywords: vbaac10.chm13734
f1_keywords:
- vbaac10.chm13734
ms.prod: access
api_name:
- Access.Report.PrintCount
ms.assetid: 9228d6eb-872c-db58-b316-78bff8b375dc
ms.date: 03/20/2019
ms.localizationpriority: medium
---


# Report.PrintCount property (Access)

Use the **PrintCount** property to identify the number of times the **OnPrint** property has been evaluated for the current section of a report. Read/write **Integer**.


## Syntax

_expression_.**PrintCount**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

Use this property only in a macro or an [event procedure](../access/Concepts/Settings/set-properties-by-using-visual-basic.md) specified by a section's **OnPrint** property setting.

Microsoft Access increments the **PrintCount** property each time the **OnPrint** property setting is evaluated for the current section. As the next section is printed, Access resets the **PrintCount** property to 0.

This property isn't available in report Design view.

The **PrintCount** property is incremented, for example, when the **[KeepTogether](Access.Section.KeepTogether.md)** property is set to No for the current section and the section is printed on more than one page. If you print a report containing order information, you might keep a running total of the order amounts.


## Example

The following example shows how you can use the **PrintCount** property to make sure that the value in the **OrderAmount** control is added only once to the running total.

**RunningTotal** can be a public variable or the name of an unbound control that is incremented each time a section is printed.

```vb
Private Sub Detail_Format(Cancel As Integer, FormatCount As Integer) 
 If PrintCount = 1 Then 
 RunningTotal = RunningTotal + OrderAmount 
 End If 
End Sub
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]