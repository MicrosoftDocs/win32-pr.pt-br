---
description: usar Windows GDI+ para desenhar em uma impressora é semelhante ao uso de GDI+ para desenhar em uma tela de computador. Para desenhar em uma impressora, obtenha um identificador de contexto de dispositivo para a impressora e, em seguida, passe esse identificador para um construtor de gráficos.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Envio da saída GDI+ para uma impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51116e27f3ef4e457d2d3cf8d39b26c1a5e2275da4b964bd4de58ec273db1e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943776"
---
# <a name="sending-gdi-output-to-a-printer"></a>Envio da saída GDI+ para uma impressora

usar Windows GDI+ para desenhar em uma impressora é semelhante ao uso de GDI+ para desenhar em uma tela de computador. Para desenhar em uma impressora, obtenha um identificador de contexto de dispositivo para a impressora e, em seguida, passe esse identificador para um construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

O aplicativo de console a seguir desenha uma linha, um retângulo e uma elipse em uma impressora chamada Myprinter:


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



no código anterior, os três GDI+ comandos de desenho estão entre chamadas para as funções [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) , sendo que cada uma recebe o identificador de contexto do dispositivo de impressora. Todos os comandos gráficos entre StartDoc e EndDoc são roteados para um metarquivo temporário. Após a chamada para EndDoc, o driver de impressora converte os dados no metarquivo no formato exigido pela impressora específica que está sendo usada.

> [!Note]  
> Se o spooling não estiver habilitado para a impressora que está sendo usada, a saída de gráficos não será roteada para um metarquivo. Em vez disso, comandos de gráficos individuais são processados pelo driver de impressora e enviados para a impressora.

 

Em geral, você não desejará embutir o nome de uma impressora como foi feito no aplicativo de console anterior. Uma alternativa para embutir o nome no código é chamar [GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obter o nome da impressora padrão. Antes de chamar GetDefaultPrinter, você deve alocar um buffer grande o suficiente para conter o nome da impressora. Você pode determinar o tamanho do buffer necessário chamando GetDefaultPrinter, passando **NULL** como o primeiro argumento.

> [!Note]  
> a função [GetDefaultPrinter](../printdocs/getdefaultprinter.md) tem suporte apenas no Windows 2000 e posterior.

 

O aplicativo de console a seguir obtém o nome da impressora padrão e, em seguida, desenha um retângulo e uma elipse nessa impressora. O [**gráfico::D chamada rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) está entre chamadas para [Startpage](/windows/win32/api/wingdi/nf-wingdi-startpage) e [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), portanto, o retângulo está em uma página por si só. Da mesma forma, a elipse está em uma página por si só.


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



 

 
