---
description: Você pode permitir que o usuário desenhe linhas com o mouse fazendo com que o procedimento de janela seja desenhado durante o processamento da \_ mensagem MOUSEMOVE do WM.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Desenho com o mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010734"
---
# <a name="drawing-with-the-mouse"></a>Desenho com o mouse

Você pode permitir que o usuário desenhe linhas com o mouse fazendo com que o procedimento de janela seja desenhado durante o processamento da mensagem [**\_ MOUSEMOVE do WM**](../inputdev/wm-mousemove.md) . O sistema envia a **mensagem \_ MOUSEMOVE do WM** para o procedimento de janela sempre que o usuário move o cursor dentro da janela. Para desenhar linhas, o procedimento de janela pode recuperar um contexto de dispositivo de exibição e desenhar uma linha na janela entre as posições de cursor atual e anterior.

No exemplo a seguir, o procedimento de janela se prepara para desenhar quando o usuário pressiona e mantém o botão esquerdo do mouse (enviando a mensagem do [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) ). À medida que o usuário move o cursor dentro da janela, o procedimento de janela recebe uma série de mensagens [**\_ MOUSEMOVE do WM**](../inputdev/wm-mousemove.md) . Para cada mensagem, o procedimento de janela desenha uma linha conectando a posição anterior e a posição atual. Para desenhar a linha, o procedimento usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para recuperar um contexto de dispositivo de exibição; em seguida, assim que o desenho for concluído e antes de retornar da mensagem, o procedimento usará a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar o contexto do dispositivo de exibição. Assim que o usuário libera o botão do mouse, o procedimento de janela limpa o sinalizador e o desenho é interrompido (o que envia a mensagem [**\_ LBUTTONUP do WM**](../inputdev/wm-lbuttonup.md) ).


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



Um aplicativo que habilita o desenho, como neste exemplo, normalmente registra os pontos ou linhas para que as linhas possam ser redesenhadas sempre que a janela for atualizada. Os aplicativos de desenho geralmente usam um contexto de dispositivo de memória e um bitmap associado para armazenar as linhas que foram desenhadas usando um mouse.

 

 
