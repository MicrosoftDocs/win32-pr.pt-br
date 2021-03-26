---
description: Usar o Windows GDI+ para desenhar em uma impressora é semelhante a usar o GDI+ para desenhar em uma tela de computador. Para desenhar em uma impressora, obtenha um identificador de contexto de dispositivo para a impressora e, em seguida, passe esse identificador para um construtor de gráficos.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Envio da saída GDI+ para uma impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c1c4f6c05e4918663284e6d7747952040dcddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010863"
---
# <a name="sending-gdi-output-to-a-printer"></a><span data-ttu-id="3d219-104">Envio da saída GDI+ para uma impressora</span><span class="sxs-lookup"><span data-stu-id="3d219-104">Sending GDI+ Output to a Printer</span></span>

<span data-ttu-id="3d219-105">Usar o Windows GDI+ para desenhar em uma impressora é semelhante a usar o GDI+ para desenhar em uma tela de computador.</span><span class="sxs-lookup"><span data-stu-id="3d219-105">Using Windows GDI+ to draw on a printer is similar to using GDI+ to draw on a computer screen.</span></span> <span data-ttu-id="3d219-106">Para desenhar em uma impressora, obtenha um identificador de contexto de dispositivo para a impressora e, em seguida, passe esse identificador para um construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="3d219-106">To draw on a printer, obtain a device context handle for the printer and then pass that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span>

<span data-ttu-id="3d219-107">O aplicativo de console a seguir desenha uma linha, um retângulo e uma elipse em uma impressora chamada Myprinter:</span><span class="sxs-lookup"><span data-stu-id="3d219-107">The following console application draws a line, a rectangle, and an ellipse on a printer named MyPrinter:</span></span>


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

   // Get a device context for the printer.
   HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\print1"), NULL, NULL);

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   StartDoc(hdcPrint, &docInfo);
   StartPage(hdcPrint);
      Graphics* graphics = new Graphics(hdcPrint);
      Pen* pen = new Pen(Color(255, 0, 0, 0));
      graphics->DrawLine(pen, 50, 50, 350, 550);
      graphics->DrawRectangle(pen, 50, 50, 300, 500);
      graphics->DrawEllipse(pen, 50, 50, 300, 500);
      delete pen;
      delete graphics;
   EndPage(hdcPrint);
   EndDoc(hdcPrint);
   
   DeleteDC(hdcPrint);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="3d219-108">No código anterior, os três comandos de desenho GDI+ estão entre chamadas para as funções [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) , sendo que cada uma recebe o identificador de contexto do dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="3d219-108">In the preceding code, the three GDI+ drawing commands are in between calls to the [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) functions, each of which receives the printer device context handle.</span></span> <span data-ttu-id="3d219-109">Todos os comandos gráficos entre StartDoc e EndDoc são roteados para um metarquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="3d219-109">All graphics commands between StartDoc and EndDoc are routed to a temporary metafile.</span></span> <span data-ttu-id="3d219-110">Após a chamada para EndDoc, o driver de impressora converte os dados no metarquivo no formato exigido pela impressora específica que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="3d219-110">After the call to EndDoc, the printer driver converts the data in the metafile into the format required by the specific printer being used.</span></span>

> [!Note]  
> <span data-ttu-id="3d219-111">Se o spooling não estiver habilitado para a impressora que está sendo usada, a saída de gráficos não será roteada para um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="3d219-111">If spooling is not enabled for the printer being used, the graphics output is not routed to a metafile.</span></span> <span data-ttu-id="3d219-112">Em vez disso, comandos de gráficos individuais são processados pelo driver de impressora e enviados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="3d219-112">Instead, individual graphics commands are processed by the printer driver and then sent to the printer.</span></span>

 

<span data-ttu-id="3d219-113">Em geral, você não desejará embutir o nome de uma impressora como foi feito no aplicativo de console anterior.</span><span class="sxs-lookup"><span data-stu-id="3d219-113">Generally you won't want to hard-code the name of a printer as was done in the preceding console application.</span></span> <span data-ttu-id="3d219-114">Uma alternativa para embutir o nome no código é chamar [GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obter o nome da impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="3d219-114">One alternative to hard-coding the name is to call [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to obtain the name of the default printer.</span></span> <span data-ttu-id="3d219-115">Antes de chamar GetDefaultPrinter, você deve alocar um buffer grande o suficiente para conter o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="3d219-115">Before you call GetDefaultPrinter, you must allocate a buffer large enough to hold the printer name.</span></span> <span data-ttu-id="3d219-116">Você pode determinar o tamanho do buffer necessário chamando GetDefaultPrinter, passando **NULL** como o primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="3d219-116">You can determine the size of the required buffer by calling GetDefaultPrinter, passing **NULL** as the first argument.</span></span>

> [!Note]  
> <span data-ttu-id="3d219-117">A função [GetDefaultPrinter](../printdocs/getdefaultprinter.md) tem suporte apenas no Windows 2000 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d219-117">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 

<span data-ttu-id="3d219-118">O aplicativo de console a seguir obtém o nome da impressora padrão e, em seguida, desenha um retângulo e uma elipse nessa impressora.</span><span class="sxs-lookup"><span data-stu-id="3d219-118">The following console application gets the name of the default printer and then draws a rectangle and an ellipse on that printer.</span></span> <span data-ttu-id="3d219-119">O [**gráfico::D chamada rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) está entre chamadas para [Startpage](/windows/win32/api/wingdi/nf-wingdi-startpage) e [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), portanto, o retângulo está em uma página por si só.</span><span class="sxs-lookup"><span data-stu-id="3d219-119">The [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call is in between calls to [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) and [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), so the rectangle is on a page by itself.</span></span> <span data-ttu-id="3d219-120">Da mesma forma, a elipse está em uma página por si só.</span><span class="sxs-lookup"><span data-stu-id="3d219-120">Similarly, the ellipse is on a page by itself.</span></span>


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

   DWORD size;
   HDC hdcPrint;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the size of the default printer name.
   GetDefaultPrinter(NULL, &size);

   // Allocate a buffer large enough to hold the printer name.
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

      StartDoc(hdcPrint, &docInfo);
         Graphics* graphics;
         Pen* pen = new Pen(Color(255, 0, 0, 0));

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawRectangle(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawEllipse(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         delete pen;
      EndDoc(hdcPrint);

      DeleteDC(hdcPrint);
   }

   delete buffer;

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
