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
# <a name="optimizing-printing-by-providing-a-printer-handle"></a><span data-ttu-id="ced5d-103">Otimizar a impressão fornecendo um identificador de impressora</span><span class="sxs-lookup"><span data-stu-id="ced5d-103">Optimizing Printing by Providing a Printer Handle</span></span>

<span data-ttu-id="ced5d-104">Um dos construtores para a classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recebe um identificador de contexto de dispositivo e um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="ced5d-104">One of the constructors for the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class receives a device context handle and a printer handle.</span></span> <span data-ttu-id="ced5d-105">Quando você envia comandos do Windows GDI+ para determinadas impressoras PostScript, o desempenho será melhor se você criar o objeto **gráfico** com esse construtor específico.</span><span class="sxs-lookup"><span data-stu-id="ced5d-105">When you send Windows GDI+ commands to certain PostScript printers, the performance will be better if you create your **Graphics** object with that particular constructor.</span></span>

<span data-ttu-id="ced5d-106">O aplicativo de console a seguir chama [GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obter o nome da impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="ced5d-106">The following console application calls [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to get the name of the default printer.</span></span> <span data-ttu-id="ced5d-107">O código passa o nome da impressora para [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) para obter um identificador de contexto de dispositivo para a impressora.</span><span class="sxs-lookup"><span data-stu-id="ced5d-107">The code passes the printer name to [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) to obtain a device context handle for the printer.</span></span> <span data-ttu-id="ced5d-108">O código também passa o nome da impressora para [OpenPrinter](../printdocs/openprinter.md) para obter um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="ced5d-108">The code also passes the printer name to [OpenPrinter](../printdocs/openprinter.md) to obtain a printer handle.</span></span> <span data-ttu-id="ced5d-109">O identificador de contexto do dispositivo e o identificador da impressora são passados para o construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ced5d-109">Both the device context handle and the printer handle are passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="ced5d-110">Em seguida, duas figuras são desenhadas na impressora.</span><span class="sxs-lookup"><span data-stu-id="ced5d-110">Then two figures are drawn on the printer.</span></span>

> [!Note]  
> <span data-ttu-id="ced5d-111">A função [GetDefaultPrinter](../printdocs/getdefaultprinter.md) tem suporte apenas no Windows 2000 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ced5d-111">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 


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



 

 
