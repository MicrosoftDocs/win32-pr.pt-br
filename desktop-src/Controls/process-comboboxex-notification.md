---
title: Como processar notificações do ComboBoxEx
description: Este tópico demonstra como processar mensagens de notificação ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917825"
---
# <a name="how-to-process-comboboxex-notifications"></a>Como processar notificações do ComboBoxEx

Este tópico demonstra como processar mensagens de notificação ComboBoxEx.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Um controle ComboBoxEx notifica sua janela pai de eventos enviando mensagens de [**\_ notificação do WM**](wm-notify.md) . Ele também passa as mensagens de notificação do [**\_ comando do WM**](/windows/desktop/menurc/wm-command) recebidas da caixa de combinação contida nela para a janela pai a ser processada. Portanto, seu aplicativo deve estar preparado para processar mensagens de **\_ notificação do WM** nas mensagens **de \_ comando** ComboBoxEx e WM que são encaminhadas do controle da caixa de combinação filho ComboBoxEx.

O exemplo nesta seção manipula as mensagens de [**\_ comando**](/windows/desktop/menurc/wm-command) do WM [**\_ Notify**](wm-notify.md) e do WM de um controle ComboBoxEx chamando uma função definida pelo aplicativo correspondente para processar essas mensagens.

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

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 