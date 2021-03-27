---
description: Para responder a uma \_ mensagem do WM Paint, use um código semelhante ao seguinte.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Pintando em um controlador de domínio que abrange vários monitores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5b1b85c8aab20b7ef2415c1d67188ecab7728c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502408"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Pintando em um controlador de domínio que abrange vários monitores

Para responder a uma mensagem do **WM \_ Paint** , use um código semelhante ao seguinte.


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



Para pintar a metade superior de uma janela, use um código semelhante ao seguinte.


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



Para pintar toda a tela virtual de forma ideal para cada monitor, use um código semelhante ao seguinte.


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



