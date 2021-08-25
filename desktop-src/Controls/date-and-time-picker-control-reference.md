---
title: Seletor de data e hora
description: Esta seção contém informações sobre os elementos de API usados com os controles de seletor de data e hora.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b29aa1bf7552b87f18a9ded05b67fc8e47770c01431af4da897f2b9733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929476"
---
# <a name="date-and-time-picker"></a>Seletor de data e hora

Esta seção contém informações sobre os elementos de API usados com os controles de seletor de data e hora.

### <a name="overviews"></a>Visões gerais



| Tópico                                                                    | Sumário                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre os controles de seletor de data e hora](date-and-time-picker-controls.md) | Um *controle de data e hora (DTP)* fornece uma interface simples e intuitiva por meio da qual as informações de data e hora do Exchange são trocadas por um usuário.<br/> |
| [Usando controles de seletor de data e hora](using-date-and-time-picker.md)    | Esta seção fornece informações e código de exemplo para implementação de controles de seletor de data e hora. <br/>                                                |



 

### <a name="macros"></a>Macros



| Tópico                                                                     | Sumário                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CloseMonthCal DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Fecha o controle do seletor de data e hora (DTP). Use esta macro ou envie a mensagem [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md) explicitamente.<br/>                                                                                                                     |
| [**\_GetDateTimePickerInfo DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Obtém informações para um controle do seletor de data e hora (DTP) especificado.<br/>                                                                                                                                                                                              |
| [**\_GetIdealSize DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Obtém o tamanho necessário para exibir o controle sem recorte. Use esta macro ou envie a mensagem [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md) explicitamente.<br/>                                                                                                        |
| [**\_GetMonthCal DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Obtém o identificador de um controle de calendário do mês filho do seletor de data e hora (DTP). Você pode usar essa macro ou enviar a mensagem [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) explicitamente. <br/>                                                                               |
| [**\_GetMonthCalColor DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Obtém a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode usar essa macro ou enviar a mensagem [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md) explicitamente. <br/>                                                           |
| [**\_GetMonthCalFont DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Obtém a fonte em que o controle de calendário do mês filho do controle de data e hora (DTP) está sendo usado no momento. Você pode usar essa macro ou enviar a mensagem [**DTM \_ GETMCFONT**](dtm-getmcfont.md) explicitamente. <br/>                                                      |
| [**\_GetMonthCalStyle DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Obtém o estilo de um controle DTP especificado. Use esta macro ou envie a mensagem [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md) explicitamente.<br/>                                                                                                                               |
| [**DataRange de DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Obtém os tempos de sistema mínimo e máximo permitidos no momento para um controle do seletor de data e hora (DTP). Você pode usar essa macro ou enviar a mensagem [**\_ GetRange DTM**](dtm-getrange.md) explicitamente. <br/>                                                              |
| [**DateTime \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Obtém a hora atualmente selecionada de um controle de data e hora (DTP) e o coloca em uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Você pode usar essa macro ou enviar a mensagem [**DTM \_ GetSystemTime**](dtm-getsystemtime.md) explicitamente. <br/> |
| [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Define a exibição de um controle DTP (data e hora) com base em uma determinada cadeia de caracteres de formato. Você pode usar essa macro ou enviar a [**mensagem \_ SetFormat DTM**](dtm-setformat.md) explicitamente. <br/>                                                                          |
| [**\_SetMonthCalColor DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Define a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode usar essa macro ou enviar a mensagem [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md) explicitamente. <br/>                                                           |
| [**\_SetMonthCalFont DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Define a fonte a ser usada pelo controle de calendário do mês filho do controle do seletor de data e hora (DTP). Você pode usar essa macro ou enviar explicitamente a mensagem [**DTM \_ SETMCFONT**](dtm-setmcfont.md) . <br/>                                                                |
| [**\_SetMonthCalStyle DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Define o estilo para um controle DTP especificado. Use esta macro ou envie a mensagem [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md) explicitamente.<br/>                                                                                                                              |
| [**SetRange de DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Define os tempos mínimos e máximos de sistema permitidos para um controle do seletor de data e hora (DTP). Você pode usar essa macro ou enviar a [**mensagem \_ SETRANGE DTM**](dtm-setrange.md) explicitamente. <br/>                                                                       |
| [**Data e hora do DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Define um controle DTP (data and time Picker) para uma determinada data e hora. Você pode usar essa macro ou enviar a mensagem [**DTM \_ SetSystemTime**](dtm-setsystemtime.md) explicitamente. <br/>                                                                                       |



 

### <a name="messages"></a>Mensagens



| Tópico                                                           | Sumário                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md)                 | Fecha um controle DTP. Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .<br/>                                                                                                                                        |
| [**DTM \_ GETDATETIMEPICKERINFO**](dtm-getdatetimepickerinfo.md) | Obtém informações sobre um controle do seletor de data e hora (DTP).<br/>                                                                                                                                                                                                                  |
| [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md)                   | Obtém o tamanho necessário para exibir o controle sem recorte. Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .<br/>                                                                                                  |
| [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md)                       | Obtém a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) . <br/>                                              |
| [**DTM \_ GETMCFONT**](dtm-getmcfont.md)                         | Obtém a fonte em que o controle de calendário do mês filho do controle de data e hora (DTP) está sendo usado no momento. Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) . <br/>                                         |
| [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md)                       | Obtém o estilo de um controle DTP. Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .<br/>                                                                                                                       |
| [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)                     | Obtém o identificador de um controle de calendário do mês filho do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) . <br/>                                                                              |
| [**GetRange DTM \_**](dtm-getrange.md)                           | Obtém os tempos de sistema mínimo e máximo permitidos no momento para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetRange de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) . <br/>                                                              |
| [**DTM \_ GETsystemtime**](dtm-getsystemtime.md)                 | Obtém a hora atualmente selecionada de um controle de data e hora (DTP) e o coloca em uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) . <br/> |
| [**DTM \_ SETformat**](dtm-setformat.md)                         | Define a exibição de um controle DTP (data e hora) com base em uma determinada cadeia de caracteres de formato. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetFormat de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) . <br/>                                                                         |
| [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md)                       | Define a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) . <br/>                                              |
| [**DTM \_ SETMCFONT**](dtm-setmcfont.md)                         | Define a fonte a ser usada pelo controle de calendário do mês filho do controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .<br/>                                                    |
| [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md)                       | Define o estilo de um controle DTP. Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .<br/>                                                                                                                       |
| [**\_SETRANGE DTM**](dtm-setrange.md)                           | Define os tempos mínimos e máximos de sistema permitidas para um controle DTP (selador de data e hora). Você pode enviar essa mensagem explicitamente ou usar a [**macro DateTime \_ SetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) <br/>                                                                      |
| [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md)                 | Define a hora em um controle DTP (selador de data e hora). Você pode enviar essa mensagem explicitamente ou usar a [**macro DateTime \_ SetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) <br/>                                                                                                   |



 

### <a name="notifications"></a>Notificações



| Tópico                                                   | Sumário                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CLOSEUP de \_ DTN](dtn-closeup.md)                         | Enviado por um controle DTP (selador de data e hora) quando o usuário fecha o calendário do mês de lista listada. O calendário do mês é fechado quando o usuário escolhe uma data do calendário do mês ou clica na seta para baixo enquanto o calendário está aberto. <br/>                                                                                                      |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md)           | Enviado por um controle DTP (selador de data e hora) sempre que ocorrer uma alteração. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                                  |
| [LISTA DE \_ DTN](dtn-dropdown.md)                       | Enviado por um controle DTP (selador de data e hora) quando o usuário ativa o calendário do mês de lista listada. <br/>                                                                                                                                                                                                                                               |
| [FORMATO \_ DTN](dtn-format.md)                           | Enviado por um controle DTP (selador de data e hora) para solicitar que o texto seja exibido em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                       |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)                 | Enviado por um controle DTP (selador de data e hora) para recuperar o tamanho máximo permitida da cadeia de caracteres que será exibida em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                           |
| [DTN \_ USERSTRING](dtn-userstring.md)                   | Enviado por um controle DTP (selador de data e hora) quando um usuário termina de editar uma cadeia de caracteres no controle . Esse código de notificação só é enviado por controles DTP definidos para o estilo [**\_ APPCANPARSE do DTS.**](date-and-time-picker-control-styles.md) Essa mensagem é enviada na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [WMKEYDOWN de DTN \_](dtn-wmkeydown.md)                     | Enviado por um controle DTP (selador de data e hora) quando o usuário digita em um campo de retorno de chamada. Essa mensagem é enviada na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (data e hora)](nm-killfocus-date-time.md) | Notifica a janela pai do controle do selador de data e hora de que o controle perdeu o foco de entrada. [**NM \_ KILLFOCUS (data e hora)**](nm-killfocus-date-time.md) é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                 |
| [NM \_ SETFOCUS (data e hora)](nm-setfocus-date-time-.md)  | Notifica a janela pai do controle do selador de data e hora de que o controle recebeu o foco de entrada. [NM \_ SETFOCUS (data/hora)](nm-setfocus-date-time-.md) é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                  |



 

### <a name="structures"></a>Estruturas



| Tópico                                                  | Sumário                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Contém informações sobre um controle DTP. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Contém informações sobre uma alteração que ocorreu em um controle DTP (selador de data e hora). Essa estrutura é usada com o código de notificação [DTN \_ DATETIMECHANGE.](dtn-datetimechange.md) <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Contém informações sobre uma parte da cadeia de caracteres de formato que define um campo de retorno de chamada dentro de um controle DTP (selador de data e hora). Ele carrega a substring que define o campo de retorno de chamada e contém um buffer para receber a cadeia de caracteres que será exibida no campo de retorno de chamada. Essa estrutura é usada com o código de notificação [ \_ DTN FORMAT.](dtn-format.md) <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Contém informações sobre um campo de retorno de chamada de controle DTP (selador de data e hora). Ele contém uma substring (retirada da cadeia de caracteres de formato do controle) que define um campo de retorno de chamada. A estrutura recebe o tamanho máximo permitida do texto que será exibido no campo de retorno de chamada. Essa estrutura é usada com o código [de notificação DTN \_ FORMATQUERY.](dtn-formatquery.md) <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Contém informações específicas de uma operação de edição que ocorreu em um controle DTP (selador de data e hora). Essa mensagem é usada com o código de notificação [DTN \_ USERSTRING.](dtn-userstring.md) <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Carrega informações usadas para descrever e manipular um código de notificação [ \_ WMKEYDOWN de DTN.](dtn-wmkeydown.md) <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Constantes



| Tópico                                                                          | Sumário                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Estilos de controle do selador de data e hora](date-and-time-picker-control-styles.md) | Os estilos de janela listados aqui são específicos para controles de selador de data e hora.<br/> |



 

 

