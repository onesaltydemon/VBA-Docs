---
title: Label.ForeTint property (Access)
keywords: vbaac10.chm14605
f1_keywords:
- vbaac10.chm14605
ms.prod: access
api_name:
- Access.Label.ForeTint
ms.assetid: cce432e8-44eb-d30c-04e2-b4e3861ecec7
ms.date: 03/01/2019
ms.localizationpriority: medium
---


# Label.ForeTint property (Access)

Gets or sets the tint that is applied to the theme color in the **ForeColor** property of the specified object. Read/write **Single**.


## Syntax

_expression_.**ForeTint**

_expression_ A variable that represents a **[Label](Access.Label.md)** object.


## Remarks

The **ForeTint** property contains a numeric expression that can be used to lighten the theme color in the **ForeColor** property. The default value of the **ForeTint** property is 100, which is neutral, and does not change the theme color.

To lighten the color, first determine the percentage by which to lighten from 1 to 100, and then subtract that value as a whole number from 100 and use the remainder. For example, to lighten the theme color by 75%, subtract 75 from 100 and use the remainder, which is 25.

This property is not surfaced in the property sheet.


## Example

The following code example lightens the **ForeColor** property by 75%.

```vb
Me.ctl.ForeTint=25
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]