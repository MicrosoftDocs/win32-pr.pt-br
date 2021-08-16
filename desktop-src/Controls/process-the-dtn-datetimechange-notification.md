---
title: Como processar a notificação de DTN_DATETIMECHANGE
description: Este tópico demonstra como processar a notificação de alterações, feitas pelo usuário, para o controle do seletor de data e hora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9490059a202eff69a05b34a086e74d6df52758713fd5b66d899d1ab114a31040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829917"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Como processar a notificação DTN \_ DATETIMECHANGE

Este tópico demonstra como processar a notificação de alterações, feitas pelo usuário, para o controle do seletor de data e hora (DTP).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções


Um controle DTP envia o código de notificação [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) sempre que ocorre uma alteração. Por exemplo, essa notificação será gerada quando o usuário alterar um dos campos no controle ou, no caso em que o controle está definido como o estilo [**DTS \_ mynone**](date-and-time-picker-control-styles.md) , quando o usuário altera o estado da caixa de seleção do controle.

Seu aplicativo deve incluir código para processar \_ mensagens DTN DATETIMECHANGE enviadas pelo controle DTP.

O exemplo de código C++ a seguir é uma função definida pelo aplicativo projetada para indicar o estado de um controle DTP que é definido para o estilo **DTS \_ All None** .



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de seletor de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do seletor de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Seletor de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




