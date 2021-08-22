---
title: Como processar mensagens de notificação da barra de faixas
description: As barras de faixa notificam a janela pai das ações do usuário enviando ao pai uma mensagem WM \_ HSCROLL ou WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211a468c5c107a96fc6b28d12feed219799450828db07be87cd8887b5816bd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540316"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Como processar mensagens de notificação da barra de faixas

As barras de faixa notificam a janela pai das ações do usuário enviando ao pai uma mensagem [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="process-trackbar-notification-messages"></a>Processar mensagens de notificação da barra de faixas

O exemplo de código a seguir é uma função que é chamada quando a janela pai da barra de faixa recebe uma [**mensagem WM \_ HSCROLL.**](wm-hscroll.md) A barra de faixa neste exemplo tem o [**estilo TBS \_ ENABLESELRANGE.**](trackbar-control-styles.md) A posição do controle deslizante é comparada ao intervalo de seleção e o controle deslizante é movido para a posição inicial ou final do intervalo de seleção quando necessário.


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

Uma caixa de diálogo que contém uma barra de faixa de estilo [**\_ TBS VERT**](trackbar-control-styles.md) pode usar essa função quando recebe uma mensagem [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles trackbar](using-trackbar-controls.md)
</dt> </dl>

 

 




