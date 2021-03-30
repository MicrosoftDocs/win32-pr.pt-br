---
title: Como processar mensagens de notificação TrackBar
description: Trackbars Notifique a janela pai das ações do usuário enviando a mensagem pai a WM \_ HSCROLL ou WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635404"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Como processar mensagens de notificação TrackBar

Trackbars Notifique a janela pai das ações do usuário enviando a mensagem pai a [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="process-trackbar-notification-messages"></a>Processar mensagens de notificação TrackBar

O exemplo de código a seguir é uma função que é chamada quando a janela pai do TrackBar recebe uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) . O TrackBar neste exemplo tem o estilo [**\_ ENABLESELRANGE TBS**](trackbar-control-styles.md) . A posição do controle deslizante é comparada ao intervalo de seleção e o controle deslizante é movido para a posição inicial ou final do intervalo de seleção, quando necessário.


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a>Comentários

Uma caixa de diálogo que contém um TrackBar de estilo [**\_ vertical do TBS**](trackbar-control-styles.md) pode usar essa função quando recebe uma mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




