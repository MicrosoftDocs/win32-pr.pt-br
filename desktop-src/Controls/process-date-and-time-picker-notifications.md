---
title: Como processar notificações de selador de data e hora
description: Esta seção demonstra como processar notificações do se picker de data e hora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81846d22f3c946d1bfdf661823429fd092b78647cf0ebcb0d683d2600ddcaf17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540469"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Como processar notificações de selador de data e hora

Esta seção demonstra como processar notificações do se picker de data e hora.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Um controle DTP (selador de data e hora) envia mensagens de notificação para a janela pai quando eventos, geralmente disparados pela entrada do usuário, ocorrem no controle . Seu aplicativo deve incluir código para determinar o tipo de mensagem de notificação e responder adequadamente.

Se você planeja usar campos de retorno de chamada com os controles DTP em seu aplicativo, deve estar preparado para lidar com códigos de notificação [DTN \_ FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)e [DTN \_ WMKEYDOWN.](dtn-wmkeydown.md) Para obter informações adicionais sobre campos de retorno de chamada, consulte [Campos de retorno de chamada](date-and-time-picker-controls.md).

O exemplo de código C++ a seguir identifica a mensagem de notificação enviada por um controle DTP e chama a função definida pelo aplicativo apropriada. Consulte os tópicos a seguir para ver exemplos de código que ilustram como processar as notificações que aparecem neste exemplo.

|   Tópicos                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [Como processar a notificação DTN \_ DATETIMECHANGE](process-the-dtn-datetimechange-notification.md) |
| [Como processar a notificação DTN \_ FORMATQUERY](process-the-dtn-formatquery-notification.md)       |
| [Como processar a notificação de formato \_ DTN](process-the-dtn-format-notfication.md)                  |
| [Como processar a notificação wmkeydown de DTN \_](process-the-dtn-wmkeydown-notification.md)           |



 



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

[Notificações de selador de data e hora](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Referência de controle do selador de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Usando controles de selador de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Selador de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




