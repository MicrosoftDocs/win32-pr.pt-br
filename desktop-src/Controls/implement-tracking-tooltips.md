---
title: Como implementar dicas de ferramentas de rastreamento
description: As dicas de ferramentas de rastreamento permanecem visíveis até que sejam explicitamente fechadas pelo aplicativo e podem alterar a posição na tela dinamicamente. Eles têm suporte da versão 4,70 e posterior dos controles comuns.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005088"
---
# <a name="how-to-implement-tracking-tooltips"></a>Como implementar dicas de ferramentas de rastreamento

As dicas de ferramentas de rastreamento permanecem visíveis até que sejam explicitamente fechadas pelo aplicativo e podem alterar a posição na tela dinamicamente. Eles têm suporte da [versão 4,70](common-control-versions.md) e posterior dos controles comuns.

Para criar uma dica de ferramenta de rastreamento, inclua o sinalizador de faixa de TTF \_ no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ao enviar a mensagem [**TTM \_ addferramenta**](ttm-addtool.md) .

Seu aplicativo deve ativar (Mostrar) e desativar (ocultar) manualmente uma dica de ferramenta de rastreamento enviando uma mensagem [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md) . Enquanto uma dica de ferramenta de rastreamento está ativa, seu aplicativo deve especificar o local da dica de ferramenta enviando mensagens [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) para o controle ToolTip. Como o aplicativo lida com tarefas como posicionar a dica de ferramenta, o rastreamento de dicas de ferramenta não usa o sinalizador de **\_ subclasse ttf** ou a mensagem [**TTM \_ RELAYEVENT**](ttm-relayevent.md) .

A mensagem [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) faz com que o controle ToolTip Exiba a janela usando um dos dois estilos de posicionamento:

-   Por padrão, a dica de ferramentas é exibida ao lado da ferramenta correspondente em uma posição que o controle escolhe. O local escolhido é relativo às coordenadas que você fornece usando essa mensagem.
-   Se você incluir o **valor \_ absoluto de TTF** no membro da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , a dica de ferramenta será exibida no local do pixel especificado na mensagem. Nesse caso, o controle não tenta alterar o local da janela de dica de ferramenta das coordenadas que você fornece.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="implement-in-place-tooltips"></a>Implementar dicas de ferramentas de In-Place

O membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que é usada no exemplo inclui o sinalizador **\_ Absolute de TTF** . Sem esse sinalizador, o controle ToolTip escolhe onde exibir a dica de ferramenta, e sua posição relativa à caixa de diálogo pode mudar repentinamente à medida que o ponteiro do mouse se move.

> [!Note]  
> `g_toolItem` é uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) global.

 

O exemplo a seguir demonstra como criar um controle de dica de ferramenta de rastreamento. O exemplo especifica a área inteira do cliente da janela principal como a ferramenta.


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a>Implementação de procedimento de janela

Quando o ponteiro do mouse estiver dentro da área do cliente, a dica de ferramenta estará ativa e exibirá as coordenadas do cursor, conforme mostrado na ilustração a seguir.

![captura de tela de uma caixa de diálogo; uma dica de ferramenta mostra as coordenadas x e y do ponteiro do mouse](images/tt-tracking.png)

O código de exemplo a seguir é do procedimento de janela para uma caixa de diálogo que exibe a dica de ferramenta de rastreamento criada no exemplo anterior. A variável booliana global *g \_ TrackingMouse* é usada para determinar se é necessário reativar a dica de ferramenta e redefinir o controle do mouse para que o aplicativo seja notificado quando o ponteiro do mouse sair da área do cliente da caixa de diálogo.


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 

 




