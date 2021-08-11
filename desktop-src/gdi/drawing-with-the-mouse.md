---
description: Você pode permitir que o usuário desenhe linhas com o mouse fazendo com que o procedimento de janela seja desenhar durante o processamento da mensagem WM \_ MOUSEMOVE.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Desenhando com o Mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de7c75c768dcdd330e04a0877bacf59b63d59a6eeb9707011faff6a6b15055c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250398"
---
# <a name="drawing-with-the-mouse"></a>Desenhando com o Mouse

Você pode permitir que o usuário desenhe linhas com o mouse fazendo com que o procedimento de janela seja desenhar durante o processamento da mensagem [**WM \_ MOUSEMOVE.**](../inputdev/wm-mousemove.md) O sistema envia a **mensagem WM \_ MOUSEMOVE** para o procedimento de janela sempre que o usuário move o cursor dentro da janela. Para desenhar linhas, o procedimento de janela pode recuperar um contexto de dispositivo de exibição e desenhar uma linha na janela entre as posições de cursor atuais e anteriores.

No exemplo a seguir, o procedimento de janela se prepara para desenhar quando o usuário pressiona e mantém o botão esquerdo do mouse (enviando a mensagem [**WM \_ LBUTTONDOWN).**](../inputdev/wm-lbuttondown.md) À medida que o usuário move o cursor dentro da janela, o procedimento de janela recebe uma série de mensagens [**WM \_ MOUSEMOVE.**](../inputdev/wm-mousemove.md) Para cada mensagem, o procedimento de janela desenha uma linha que conecta a posição anterior e a posição atual. Para desenhar a linha, o procedimento usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para recuperar um contexto de dispositivo de exibição; em seguida, assim que o desenho for concluído e antes de retornar da mensagem, o procedimento usará a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar o contexto do dispositivo de exibição. Assim que o usuário libera o botão do mouse, o procedimento de janela limpa o sinalizador e o desenho para (que envia a mensagem [**WM \_ LBUTTONUP).**](../inputdev/wm-lbuttonup.md)


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



Um aplicativo que permite o desenho, como neste exemplo, normalmente registra os pontos ou linhas para que as linhas possam ser redesenhadas sempre que a janela for atualizada. Os aplicativos de desenho geralmente usam um contexto de dispositivo de memória e um bitmap associado para armazenar linhas que foram desenhadas usando um mouse.

 

 
