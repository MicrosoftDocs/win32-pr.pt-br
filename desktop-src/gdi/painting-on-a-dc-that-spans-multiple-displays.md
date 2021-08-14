---
description: Para responder a uma mensagem WM \_ PAINT, use código como o seguinte.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Pintura em um DC que abrange várias exibições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550279d003c7d32fc97923ea6ebe4c95364773e514a69e4c66bdb4b100784384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759477"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Pintura em um DC que abrange várias exibições

Para responder a uma **mensagem WM \_ PAINT,** use código como o seguinte.


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



Para pintar a metade superior de uma janela, use código como o seguinte.


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



Para pintar a tela virtual inteira de forma ideal para cada monitor, use código como o seguinte.


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



