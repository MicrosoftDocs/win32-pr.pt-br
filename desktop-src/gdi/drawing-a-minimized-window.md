---
description: Você pode desenhar suas próprias janelas minimizadas em vez de fazer com que o sistema as desenhe para você.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Desenhando uma janela minimizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370671"
---
# <a name="drawing-a-minimized-window"></a>Desenhando uma janela minimizada

Você pode desenhar suas próprias janelas minimizadas em vez de fazer com que o sistema as desenhe para você. A maioria dos aplicativos define um ícone de classe ao registrar a classe Window para a janela, e o sistema desenha o ícone quando a janela é minimizada. No entanto, se você definir o ícone de classe como **nulo**, o sistema enviará uma mensagem de [**\_ pintura do WM**](wm-paint.md) para o procedimento de janela sempre que a janela for minimizada, permitindo que o procedimento de janela desenhe na janela minimizada.

No exemplo a seguir, o procedimento de janela desenha uma estrela na janela minimizada. O procedimento usa a função [**Isicony**](/windows/win32/api/winuser/nf-winuser-isiconic) para determinar quando a janela é minimizada. Isso garante que a estrela seja desenhada somente quando a janela for minimizada.


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



Você define o ícone de classe como **nulo** definindo o membro **HIcon** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) como **NULL** antes de chamar a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) para a classe Window.

 

 
