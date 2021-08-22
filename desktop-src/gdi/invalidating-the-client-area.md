---
description: O sistema não é a única fonte de mensagens WM \_ PAINT. A função InvalidateRect ou InvalidateRgn pode gerar indiretamente mensagens WM \_ PAINT para suas janelas. Essas funções marcam toda ou parte de uma área de cliente como inválida (que deve ser redesenhada).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidando a área do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94a3a5b4e6903c549331788f9e81947dca44e7a699bb1a633bce46525585b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558656"
---
# <a name="invalidating-the-client-area"></a>Invalidando a área do cliente

O sistema não é a única fonte de [**mensagens WM \_ PAINT.**](wm-paint.md) A [**função InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) pode gerar indiretamente **mensagens WM \_ PAINT** para suas janelas. Essas funções marcam toda ou parte de uma área de cliente como inválida (que deve ser redesenhada).

No exemplo a seguir, o procedimento de janela invalida toda a área do cliente ao processar mensagens [**WM \_ CHAR.**](../inputdev/wm-char.md) Isso permite que o usuário altere a figura digitando um número e exibindo os resultados; esses resultados são desenhados assim que não há nenhuma outra mensagem na fila de mensagens do aplicativo.


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



Neste exemplo, o **argumento NULL** usado [**por InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) especifica toda a área do cliente; o **argumento TRUE** faz com que o plano de fundo seja apagado. Se você não quiser que o aplicativo aguarde até que a fila de mensagens do aplicativo não tenha outras mensagens, use a [**função UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) para forçar a mensagem [**WM \_ PAINT**](wm-paint.md) a ser enviada imediatamente. Se houver alguma parte inválida da área do cliente, **UpdateWindow** enviará a mensagem **WM \_ PAINT** para a janela especificada diretamente para o procedimento de janela.

 

 
