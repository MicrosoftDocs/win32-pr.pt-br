---
title: Como processar notificações do ComboBoxEx
description: Este tópico demonstra como processar mensagens de notificação do ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ec73c31020283afe5876567a57fc1fbd8a23cee123e9dc417c14c57a86709a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575486"
---
# <a name="how-to-process-comboboxex-notifications"></a>Como processar notificações do ComboBoxEx

Este tópico demonstra como processar mensagens de notificação do ComboBoxEx.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Um controle ComboBoxEx notifica sua janela pai de eventos enviando [**mensagens WM \_ NOTIFY.**](wm-notify.md) Ele também passa as mensagens de notificação [**\_ WM COMMAND**](/windows/desktop/menurc/wm-command) que recebe da caixa de combinação contida dentro dela para a janela pai a ser processada. Portanto, seu aplicativo deve estar preparado para processar mensagens **WM \_ NOTIFY** das mensagens ComboBoxEx e **WM \_ COMMAND** que são encaminhadas do controle de caixa de combinação filho ComboBoxEx.

O exemplo nesta seção trata as mensagens [**WM \_ NOTIFY**](wm-notify.md) e [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) de um controle ComboBoxEx chamando uma função definida pelo aplicativo correspondente para processar essas mensagens.

## <a name="complete-example"></a>Exemplo completo


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Referência de controle ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Usando controles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[Comboboxex](comboboxex-control-reference.md)
</dt> </dl>

 

 