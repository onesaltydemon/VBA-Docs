---
title: FileDialogFilter.Extensions property (Office)
keywords: vbaof11.chm254002
f1_keywords:
- vbaof11.chm254002
ms.prod: office
api_name:
- Office.FileDialogFilter.Extensions
ms.assetid: ee80ebef-8214-8cef-9676-e6293e5d2a3f
ms.date: 01/09/2019
ms.localizationpriority: medium
---


# FileDialogFilter.Extensions property (Office)

Gets a value containing the extensions that determine which files are displayed in a file dialog box for each **Filter** object. Read-only.


## Syntax

_expression_.**Extensions**

_expression_ An expression that returns a **[FileDialogFilter](Office.FileDialogFilter.md)** object.


## Return value

String


## Example

The following example displays the extensions and descriptions for Microsoft Excel files by iterating through the filter in the **SaveAs** dialog box.


```vb
Sub Main() 
 
 'Declare a variable as a FileDialogFilters collection. 
 Dim fdfs As FileDialogFilters 
 
 'Declare a variable as a FileDialogFilter object. 
 Dim fdf As FileDialogFilter 
 
 'Set the FileDialogFilters collection variable to 
 'the FileDialogFilters collection of the SaveAs dialog box. 
 Set fdfs = Application.FileDialog(msoFileDialogSaveAs).Filters 
 
 'Iterate through the description and extensions of each 
 'default filter in the SaveAs dialog box. 
 For Each fdf In fdfs 
 
 'Display the description of filters that include 
 'Microsoft Excel files. 
 If InStr(1, fdf.Extensions, "xls", vbTextCompare) > 0 Then 
 MsgBox "Description of filter: " & fdf.Description 
 End If 
 Next fdf 
End Sub
```


## See also

- [FileDialogFilter object members](overview/library-reference/filedialogfilter-members-office.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]