---
title: "Printing in Rich Edit Controls | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: ["cpp-windows"]
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: ["C++"]
helpviewer_keywords: ["printing [MFC], CRichEditCtrl", "rich edit controls [MFC], printing", "CRichEditCtrl class [MFC], printing"]
ms.assetid: dbda0e40-018f-424e-b5d8-7b489aaf27af
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
ms.workload: ["cplusplus"]
---
# Printing in Rich Edit Controls
You can tell a rich edit control ([CRichEditCtrl](../mfc/reference/cricheditctrl-class.md)) to render its output for a specified device, such as a printer. You can also specify the output device for which a rich edit control formats its text.  
  
 To format part of the contents of a rich edit control for a specific device, you can use the [FormatRange](../mfc/reference/cricheditctrl-class.md#formatrange) member function. The [FORMATRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787911) structure used with this function specifies the range of text to format as well as the device context (DC) for the target device.  
  
 After formatting text for an output device, you can send the output to the device by using the [DisplayBand](../mfc/reference/cricheditctrl-class.md#displayband) member function. By repeatedly using `FormatRange` and `DisplayBand`, an application that prints the contents of a rich edit control can implement banding. (Banding is division of output into smaller parts for printing purposes.)  
  
 You can use the [SetTargetDevice](../mfc/reference/cricheditctrl-class.md#settargetdevice) member function to specify the target device for which a rich edit control formats its text. This function is useful for WYSIWYG (what you see is what you get) formatting, in which an application positions text using the default printer's font metrics instead of the screen's.  
  
## See Also  
 [Using CRichEditCtrl](../mfc/using-cricheditctrl.md)   
 [Controls](../mfc/controls-mfc.md)

