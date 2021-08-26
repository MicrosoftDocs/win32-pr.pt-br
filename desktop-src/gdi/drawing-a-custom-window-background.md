---
description: Você pode desenhar seu próprio plano de fundo de janela em vez de fazer com que o sistema o desenhe para você.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Desenhando um plano de fundo de janela personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4248f7d7a1ae27ae09c93e95734fd72285028e1185b6d35110e5141fcbf88c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966006"
---
# <a name="drawing-a-custom-window-background"></a>Desenhando um plano de fundo de janela personalizada

Você pode desenhar seu próprio plano de fundo de janela em vez de fazer com que o sistema o desenhe para você. A maioria dos aplicativos especifica uma alça de pincel ou um valor de cor do sistema para o pincel de plano de fundo da classe ao registrar a classe de janela; o sistema usa o pincel ou a cor para desenhar o plano de fundo. No entanto, se você definir o pincel de plano de fundo da classe como **nulo**, o sistema enviará uma mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) para o procedimento de janela sempre que o plano de fundo da janela precisar ser desenhado, permitindo desenhar um plano de fundo personalizado.

No exemplo a seguir, o procedimento de janela desenha um padrão quadriculado grande que se ajusta perfeitamente à janela. O procedimento preenche a área do cliente com um pincel branco e, em seguida, desenha retângulos de 13 20 a 20 usando um pincel cinza. O contexto do dispositivo de vídeo a ser usado ao desenhar o plano de fundo é especificado no parâmetro *wParam* da mensagem.


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



Se o aplicativo desenhar sua própria janela minimizada, o sistema também enviará a mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) para o procedimento de janela para desenhar o plano de fundo da janela minimizada. Você pode usar a mesma técnica usada pelo [**WM \_ Paint**](wm-paint.md) para determinar se a janela está minimizada ou não, chamar a função [**isicony**](/windows/win32/api/winuser/nf-winuser-isiconic) e verificar o valor de retorno **true**.

 

 
