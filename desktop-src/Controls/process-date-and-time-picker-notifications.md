---
title: Como processar notificações de seletor de data e hora
description: Esta seção demonstra como processar notificações de seletor de data e hora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b904c464677a81151b03e3ae89085847e4e8bdf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008631"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Como processar notificações de seletor de data e hora

Esta seção demonstra como processar notificações de seletor de data e hora.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Um controle de data e hora (DTP) envia mensagens de notificação para a janela pai quando os eventos, geralmente disparados pela entrada do usuário, ocorrem no controle. Seu aplicativo deve incluir código para determinar o tipo de mensagem de notificação e responder adequadamente.

Se você planeja usar campos de retorno de chamada com os controles DTP em seu aplicativo, deverá estar preparado para manipular os códigos de notificação [DTN \_ FORMATQUERY](dtn-formatquery.md), [DTN \_ Format](dtn-format.md)e [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . Para obter informações adicionais sobre campos de retorno de chamada, consulte [campos de retorno de chamada](date-and-time-picker-controls.md).

O exemplo de código C++ a seguir identifica a mensagem de notificação enviada por um controle DTP e chama a função apropriada definida pelo aplicativo. Consulte os tópicos a seguir para obter exemplos de código que ilustram como processar as notificações que aparecem neste exemplo.

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [Como processar a notificação DTN \_ DATETIMECHANGE](process-the-dtn-datetimechange-notification.md) |
| [Como processar a notificação DTN \_ FORMATQUERY](process-the-dtn-formatquery-notification.md)       |
| [Como processar a notificação de \_ formato DTN](process-the-dtn-format-notfication.md)                  |
| [Como processar a notificação DTN \_ WMKEYDOWN](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Notificações do seletor de data e hora](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Referência de controle do seletor de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Usando controles de seletor de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Seletor de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




