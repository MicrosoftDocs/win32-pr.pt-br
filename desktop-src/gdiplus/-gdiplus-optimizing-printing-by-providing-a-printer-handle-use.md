---
description: Um dos construtores para a classe Graphics recebe um identificador de contexto de dispositivo e um identificador de impressora.
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: Otimizar a impressão fornecendo um identificador de impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967405"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a>Otimizar a impressão fornecendo um identificador de impressora

Um dos construtores para a classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recebe um identificador de contexto de dispositivo e um identificador de impressora. Quando você envia comandos do Windows GDI+ para determinadas impressoras PostScript, o desempenho será melhor se você criar o objeto **gráfico** com esse construtor específico.

O aplicativo de console a seguir chama [GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obter o nome da impressora padrão. O código passa o nome da impressora para [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) para obter um identificador de contexto de dispositivo para a impressora. O código também passa o nome da impressora para [OpenPrinter](../printdocs/openprinter.md) para obter um identificador de impressora. O identificador de contexto do dispositivo e o identificador da impressora são passados para o construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Em seguida, duas figuras são desenhadas na impressora.

> [!Note]  
> A função [GetDefaultPrinter](../printdocs/getdefaultprinter.md) tem suporte apenas no Windows 2000 e posterior.

 


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   DWORD   size;
   HDC     hdcPrint;
   HANDLE  printerHandle;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the length of the printer name.
   GetDefaultPrinter(NULL, &size);
   TCHAR* buffer = new TCHAR[size];

   // Get the printer name.
   if(!GetDefaultPrinter(buffer, &size))
   {
      printf("Failure");
   }
   else
   {
      // Get a device context for the printer.
      hdcPrint = CreateDC(NULL, buffer, NULL, NULL);

      // Get a printer handle.
      OpenPrinter(buffer, &printerHandle, NULL);

      StartDoc(hdcPrint, &docInfo);
      StartPage(hdcPrint);
         Graphics* graphics = new Graphics(hdcPrint, printerHandle);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         delete(pen);
         delete(graphics);
      EndPage(hdcPrint);
      EndDoc(hdcPrint);

      ClosePrinter(printerHandle);
      DeleteDC(hdcPrint);
   }

   delete buffer;
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
