---
description: Uma maneira de obter um identificador de contexto de dispositivo para uma impressora é exibir uma caixa de diálogo de impressão e permitir que o usuário escolha uma impressora.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Exibindo uma caixa de diálogo de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113c9235e70712a4923ebdc3ad239f533160eb2f84f76ae729d7fadf203ca612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036824"
---
# <a name="displaying-a-print-dialog-box"></a>Exibindo uma caixa de diálogo de impressão

Uma maneira de obter um identificador de contexto de dispositivo para uma impressora é exibir uma caixa de diálogo de impressão e permitir que o usuário escolha uma impressora. A função [PRINTDLG](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) (que exibe a caixa de diálogo) tem um parâmetro que é o endereço de uma estrutura [PRINTDLG](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) . A estrutura PRINTDLG tem vários membros, mas você pode deixar que a maioria deles seja definida com seus valores padrão. Os dois membros que você precisa definir são **lStructSize** e **flags**. Defina **lStructSize** como o tamanho de uma variável PRINTDLG e defina **sinalizadores** como PD \_ RETURNDC. Definir **sinalizadores** para PC \_ RETURNDC especifica que você deseja que a função PRINTDLG preencha o campo **HDC** com um identificador de contexto de dispositivo para a impressora escolhida pelo usuário.


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
   
   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";
   
   // Create a PRINTDLG structure, and initialize the appropriate fields.
   PRINTDLG printDlg;
   ZeroMemory(&printDlg, sizeof(printDlg));
   printDlg.lStructSize = sizeof(printDlg);
   printDlg.Flags = PD_RETURNDC;
   
   // Display a print dialog box.
   if(!PrintDlg(&printDlg))
   {
      printf("Failure\n");
   }
   else
   {
      // Now that PrintDlg has returned, a device context handle
      // for the chosen printer is in printDlg->hDC.
      
      StartDoc(printDlg.hDC, &docInfo);
      StartPage(printDlg.hDC);
         Graphics* graphics = new Graphics(printDlg.hDC);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         graphics->DrawLine(pen, 200, 500, 400, 650);
         delete pen;
         delete graphics;
      EndPage(printDlg.hDC);
      EndDoc(printDlg.hDC); 
   }
   if(printDlg.hDevMode) 
      GlobalFree(printDlg.hDevMode);
   if(printDlg.hDevNames) 
      GlobalFree(printDlg.hDevNames);
   if(printDlg.hDC)
      DeleteDC(printDlg.hDC);
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
