---
description: Você pode fazer com que seu aplicativo redesenhe todo o conteúdo da área do cliente sempre que a janela mudar de tamanho definindo os \_ estilos cs HREDRAW e cs \_ VREDRAW para a classe Window.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Redesenhando toda a área do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3c438fe36160f27b1015daf7874e237035f927825199b93b3a508668f40bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759142"
---
# <a name="redrawing-the-entire-client-area"></a>Redesenhando toda a área do cliente

Você pode fazer com que seu aplicativo redesenhe todo o conteúdo da área do cliente sempre que a janela mudar de tamanho definindo os \_ estilos cs HREDRAW e cs \_ VREDRAW para a classe Window. Os aplicativos que ajustam o tamanho do desenho com base no tamanho da janela usam esses estilos para garantir que eles comecem com uma área do cliente completamente vazia ao desenhar.

No exemplo a seguir, o procedimento de janela desenha uma estrela de cinco pontas que se ajusta perfeitamente na área do cliente. Ele usa um contexto de dispositivo comum e deve definir o modo de mapeamento, bem como extensões de janela e visor cada vez que a mensagem de [**\_ pintura do WM**](wm-paint.md) é processada.


```C++
LRESULT APIENTRY WndProc(HWMD hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
    RECT rc; 
    POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
    . 
    . 
    . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            GetClientRect(hwnd, &rc); 
            SetMapMode(hdc, MM_ANISOTROPIC); 
            SetWindowExtEx(hdc, 100, 100, NULL); 
            SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
            Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
        . 
        . 
        . 
} 
 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    WNDCLASS wc; 
 
    . 
    . 
    . 
 
        wc.style = CS_HREDRAW | CS_VREDRAW; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
 
    . 
    . 
    . 
 
        RegisterClass(&wc); 
 
    . 
    . 
    . 
 
    return msg.wParam; 
} 
```



 

 



