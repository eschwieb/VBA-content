---
title: LineFormat.EndArrowheadStyle Property (Excel)
keywords: vbaxl10.chm110008
f1_keywords:
- vbaxl10.chm110008
ms.prod: excel
api_name:
- Excel.LineFormat.EndArrowheadStyle
ms.assetid: 0d9eaff5-3ebc-572c-e188-d39848fa9bd2
ms.date: 06/08/2017
---


# LineFormat.EndArrowheadStyle Property (Excel)

Returns or sets the style of the arrowhead at the end of the specified line. Read/write  **[MsoArrowheadStyle](http://msdn.microsoft.com/library/e598631e-dad9-649b-767b-99e7e7ea83da%28Office.15%29.aspx)** .


## Syntax

 _expression_ . **EndArrowheadStyle**

 _expression_ A variable that represents a **LineFormat** object.


## Remarks





| **MsoArrowheadStyle** can be one of these **MsoArrowheadStyle** constants.|
| **msoArrowheadNone**|
| **msoArrowheadOval**|
| **msoArrowheadStyleMixed**|
| **msoArrowheadDiamond**|
| **msoArrowheadOpen**|
| **msoArrowheadStealth**|
| **msoArrowheadTriangle**|

## Example

This example adds a line to  `myDocument`. There's a short, narrow oval on the line's starting point and a long, wide triangle on its end point.


```vb
Set myDocument = Worksheets(1) 
With myDocument.Shapes.AddLine(100, 100, 200, 300).Line 
    .BeginArrowheadLength = msoArrowheadShort 
    .BeginArrowheadStyle = msoArrowheadOval 
    .BeginArrowheadWidth = msoArrowheadNarrow 
    .EndArrowheadLength = msoArrowheadLong 
    .EndArrowheadStyle = msoArrowheadTriangle 
    .EndArrowheadWidth = msoArrowheadWide 
End With
```


## See also


#### Concepts


[LineFormat Object](lineformat-object-excel.md)

